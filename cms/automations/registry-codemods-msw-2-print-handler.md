---
created-on: 2024-01-31T16:23:08.539Z
f_long-description: >-
  ## Description
  

  A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.
  

  
  ### Before
  
  ```ts
  
  worker.printHandlers();
  
  ```
  
  ### After
  
  ```ts
  
  worker.listHandlers().forEach((handler) => {
  	console.log(handler.info.header);
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/print-handler
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace printHandlers() calls
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.539Z
published-on: 2024-01-31T16:23:08.539Z
seo:
  title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  og:title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace printHandlers() calls | Codemod.com Automations
  description: A new way of listing all handlers is preferred in msw v2
  twitter:card: A new way of listing all handlers is preferred in msw v2
---
A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.