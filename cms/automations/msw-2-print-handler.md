---
created-on: 2023-11-16T14:11:04.212Z
f_long-description: >-
  ## Description


  A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.


  ## Example


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


  ### Links for more info


  * [msw v1 to v2 migration guide -> print handlers](https://mswjs.io/docs/migrations/1.x-to-2.x/#printhandlers)
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/print-handler
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=HvNEhmVfoqpwAcVZt7U9xaYBS2o
f_cli-command: codemod msw/2/print-handler
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: msw-print-handler
updated-on: 2023-11-17T15:17:39.056Z
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5 minutes/occurrence
date: 2023-11-20T14:53:04.294Z
f_slug-name: msw-print-handler
title: MSW V2 - Replace printHandlers() calls
published-on: 2023-11-17T15:18:58.613Z
f_labels:
  - cms/labels/msw-v1-v2.md
tags: automations
---
A new way of listing all handlers is preferred in msw v2. This codemod replaces `printHandlers()` calls with the new way of doing that.