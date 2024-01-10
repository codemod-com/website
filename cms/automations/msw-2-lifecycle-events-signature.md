---
created-on: 2024-01-10T11:59:57.447Z
f_long-description: >-
  ## Description
  

  In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.
  

  
  ### Before
  
  ```ts
  
  server.events.on("request:start", (req, reqId) => {
    doStuff(req, reqId);
  });
  
  ```
  
  ### After
  
  ```ts
  
  server.events.on("request:start", ({ request, requestId }) => {
    doStuff(request, requestId);
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/lifecycle-events-signature
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=DIAvSd9O-rhmXNGuTbHlOROvz6U
f_cli-command: intuita msw/2/lifecycle-events-signature
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-lifecycle-events-signature
title: Msw V2 - Replace lifecycle events callback signature [BETA]
f_slug-name: msw-2-lifecycle-events-signature
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.447Z
published-on: 2024-01-10T11:59:57.447Z
seo:
  title: Msw V2 - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  og:title: Msw V2 - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  twitter:title: Msw V2 - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  description: In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.
  twitter:card: In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.
---
In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.