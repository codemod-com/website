---
created-on: 2024-01-31T16:23:08.559Z
f_long-description: >-
  ## Description
  

  A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.
  

  
  ### Before
  
  ```ts
  
  rest.get('/resource', (req, res, ctx) => {
  	return req.passthrough();
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { passthrough } from 'msw';
  
  rest.get('/resource', (req, res, ctx) => {
  	return passthrough();
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/req-passthrough
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace printHandlers() calls
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5 minutes/occurence"
tags: automations
updated-on: 2024-01-31T16:23:08.559Z
published-on: 2024-01-31T16:23:08.559Z
seo:
  title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  og:title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  description: A new way of calling a passthrough is available in msw v2
  twitter:card: A new way of calling a passthrough is available in msw v2
---
A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.