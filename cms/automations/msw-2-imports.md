---
created-on: 2024-01-10T11:59:57.425Z
f_long-description: >-
  ## Description
  

  Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.
    -   `setupWorker` is now imported from `msw/browser`
    -   `rest` from `msw` is now named `http`
    -   `RestHandler` from `msw` is now named `HttpHandler`
  

  
  ### Before
  
  ```ts
  
  import { setupWorker, rest as caller, RestHandler } from 'msw';
  
  const handlers: RestHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]
  
  ```
  
  ### After
  
  ```ts
  
  import { setupWorker } from 'msw/browser';
  import { http as caller, HttpHandler } from 'msw';
  
  const handlers: HttpHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/imports
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=03s9tN6jERYILUlAfRX9cNotRpc
f_cli-command: intuita msw/2/imports
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-imports
title: Msw V2 - Replace MSW Imports
f_slug-name: msw-2-imports
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~10 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.425Z
published-on: 2024-01-10T11:59:57.425Z
seo:
  title: Msw V2 - Replace MSW Imports | Codemod.com Automations
  og:title: Msw V2 - Replace MSW Imports | Codemod.com Automations
  twitter:title: Msw V2 - Replace MSW Imports | Codemod.com Automations
  description: Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.
  twitter:card: Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.
---
Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.