---
created-on: 2024-01-31T16:23:08.469Z
f_long-description: >-
  ## Description
  

  `ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod:
    -   `ctx.fetch(req)` is replaced with `fetch(bypass(req))`.
  NOTE: The `bypass` call is meant to wrap the new `request` object available on the callback argument. This object is not being destructured in this codemod, so you will have to do it manually or run a `callback-signature` codemod that will do that and replace the reference for you.
  

  
  ### Before
  
  ```ts
  
  import { rest } from 'msw';
  
  const handlers: RestHandler[] = [
  	rest.get('/user', async (req, res, ctx) => {
  		const originalRequest = await ctx.fetch(req);
  
  		return res(ctx.json({ firstName: 'John' }));
  	}),
  ];
  
  ```
  
  ### After
  
  ```ts
  
  import { rest } from 'msw';
  
  const handlers: RestHandler[] = [
  	rest.get('/user', async (req, res, ctx) => {
  		const originalRequest = await fetch(bypass(req));
  
  		return res(ctx.json({ firstName: 'John' }));
  	}),
  ];
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/ctx-fetch
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace ctx.fetch() calls
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.469Z
published-on: 2024-01-31T16:23:08.469Z
seo:
  title: Registry Vcodemods - Replace ctx.fetch() calls | Codemod.com Automations
  og:title: Registry Vcodemods - Replace ctx.fetch() calls | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace ctx.fetch() calls | Codemod.com Automations
  description: ctx
  twitter:card: ctx
---
`ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod: