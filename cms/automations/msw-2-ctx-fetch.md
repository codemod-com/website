---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description


  `ctx.fetch(req)` is now meant to be called as `fetch(bypass(req))` where `bypass` is a new function available in the `msw` library. Changes applied by this codemod:


  * `ctx.fetch(req)` is replaced with `fetch(bypass(req))`.


  NOTE: The `bypass` call is meant to wrap the new `request` object available on the callback argument. This object is not being destructured in this codemod, so you will have to do it manually or run a `callback-signature` codemod that will do that and replace the reference for you.


  ## Example


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


  ````ts

  import { rest } from 'msw';


  const handlers: RestHandler[] = [
    rest.get('/user', async (req, res, ctx) => {
      const originalRequest = await fetch(bypass(req));

      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ``` ### Links for more info -   [msw v1 to v2 migration guide -> ctx fetch](https://mswjs.io/docs/migrations/1.x-to-2.x/#ctxfetch)

  ````
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/ctx-fetch
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=UsLIVQ68jE49SQnM9JaTvQvmGaU
f_codemod-studio-link: https://go.intuita.io/TDzFWR
f_cli-command: codemod msw/2/ctx-fetch
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: msw-ctx-fetch
updated-on: 2023-11-17T15:17:39.056Z
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
date: 2023-11-20T14:53:04.294Z
f_slug-name: msw-ctx-fetch
title: MSW V2 - Replace ctx.fetch() calls
published-on: 2023-11-17T15:18:58.613Z
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
---
This codemod replaces `ctx.fetch(req)` with `fetch(bypass(req))`.