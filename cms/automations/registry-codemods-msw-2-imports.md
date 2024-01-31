---
created-on: 2024-01-31T16:23:08.496Z
f_long-description: >-
  ## Description
  

  Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.
    -   `setupWorker` is now imported from `msw/browser`
    -   `rest` from `msw` is now named `http`
    -   `RestHandler` from `msw` is now named `HttpHandler`
  

  
  ### Before
  
  ```ts
  
  import { rest as caller, RestHandler, setupWorker } from 'msw';
  
  const handlers: RestHandler[] = [
  	caller.get('/user', (req, res, ctx) => {
  		return res(ctx.json({ firstName: 'John' }));
  	}),
  ];
  
  ```
  
  ### After
  
  ```ts
  
  import { http as caller, HttpHandler } from 'msw';
  import { setupWorker } from 'msw/browser';
  
  const handlers: HttpHandler[] = [
  	caller.get('/user', (req, res, ctx) => {
  		return res(ctx.json({ firstName: 'John' }));
  	}),
  ];
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/imports
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace MSW Imports
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~10 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.496Z
published-on: 2024-01-31T16:23:08.496Z
seo:
  title: Registry Vcodemods - Replace MSW Imports | Codemod.com Automations
  og:title: Registry Vcodemods - Replace MSW Imports | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace MSW Imports | Codemod.com Automations
  description: Following the original msw [upgrade guide](https://mswjs
  twitter:card: Following the original msw [upgrade guide](https://mswjs
---
Following the original msw [upgrade guide](https://mswjs.io/docs/migrations/1.x-to-2.x/#imports), there are certain imports that changed their location and/or naming. This codemod will adjust your imports to the new location and naming.