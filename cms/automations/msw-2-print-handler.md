---
created-on: 2024-01-10T11:59:57.465Z
f_long-description: >-
  ## Description
  

  A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.
  

  
  ### Before
  
  ```ts
  
  worker.printHandlers()
  
  ```
  
  ### After
  
  ```ts
  
  worker.listHandlers().forEach((handler) => {
    console.log(handler.info.header)
  })
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/print-handler
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=HvNEhmVfoqpwAcVZt7U9xaYBS2o
f_cli-command: intuita msw/2/print-handler
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-print-handler
title: Msw V2 - Replace printHandlers() calls
f_slug-name: msw-2-print-handler
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.465Z
published-on: 2024-01-10T11:59:57.465Z
seo:
  title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  og:title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  twitter:title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  description: A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.
  twitter:card: A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.
---
A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.