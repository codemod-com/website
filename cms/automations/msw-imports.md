---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description


  Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will import correct objects from appropriate paths to start your msw migration path.


  * `setupWorker` is now imported from `msw/browser` -   `rest` from `msw` is now named `http` -   `RestHandler` from `msw` is now named `HttpHandler`


  ## Example


  ### Before


  ```typescript

  import { setupWorker, rest as caller, RestHandler } from 'msw';

  const handlers: RestHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ```


  ### After


  ````typescript

  import { setupWorker } from 'msw/browser'; import { http as caller, HttpHandler } from 'msw';

  const handlers: HttpHandler[] = [
    caller.get('/user', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ]

  ``` ### Links for more info

  -   [msw v1 to v2 migration guide -> imports](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports)

  ````
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/msw/2/imports
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=03s9tN6jERYILUlAfRX9cNotRpc
f_codemod-studio-link: https://go.intuita.io/vUBlZL
f_cli-command: intuita msw/2/imports
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: msw-imports
updated-on: 2023-11-17T15:17:39.056Z
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 10 minutes/occurrence
date: 2023-11-20T14:53:04.294Z
f_slug-name: msw-imports
title: MSW V2 - Replace MSW Imports
published-on: 2023-11-17T15:18:58.613Z
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
---
This codemod replaces MSW v1 with v2 imports.