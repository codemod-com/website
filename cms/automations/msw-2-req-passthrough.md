---
created-on: 2024-01-10T11:59:57.483Z
f_long-description: >-
  ## Description
  

  A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.
  

  
  ### Before
  
  ```ts
  
  rest.get('/resource', (req, res, ctx) => {
    return req.passthrough()
  })
  
  ```
  
  ### After
  
  ```ts
  
  import { passthrough } from 'msw'
  
  rest.get('/resource', (req, res, ctx) => {
    return passthrough()
  })
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/req-passthrough
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=SHuKC96klArO3YKWCrmydNvoQl8
f_cli-command: intuita msw/2/req-passthrough
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-req-passthrough
title: Msw V2 - Replace printHandlers() calls
f_slug-name: msw-2-req-passthrough
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5 minutes/occurence"
tags: automations
updated-on: 2024-01-10T11:59:57.483Z
published-on: 2024-01-10T11:59:57.483Z
seo:
  title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  og:title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  twitter:title: Msw V2 - Replace printHandlers() calls | Codemod.com Automations
  description: A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.
  twitter:card: A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.
---
A new way of calling a passthrough is available in msw v2. This codemod replaces `req.passthrough()` calls with the new way of doing that using exported function.