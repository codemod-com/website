---
created-on: 2024-01-10T11:59:57.407Z
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
  ]
  
  ```
  
  ### After
  
  ```ts
  
  import { rest } from 'msw';
  
  const handlers: RestHandler[] = [
    rest.get('/user', async (req, res, ctx) => {
      const originalRequest = await fetch(bypass(req));
  
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/ctx-fetch
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=UsLIVQ68jE49SQnM9JaTvQvmGaU
f_cli-command: intuita msw/2/ctx-fetch
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-ctx-fetch
title: Msw V2 - Replace ctx.fetch() calls
f_slug-name: msw-2-ctx-fetch
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.407Z
published-on: 2024-01-10T11:59:57.407Z
seo:
  title: Msw V2 - Replace ctx.fetch() calls | Codemod.com Automations
  og:title: Msw V2 - Replace ctx.fetch() calls | Codemod.com Automations
  twitter:title: Msw V2 - Replace ctx.fetch() calls | Codemod.com Automations
  description: `ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod:
  twitter:card: `ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod:
---
`ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod: