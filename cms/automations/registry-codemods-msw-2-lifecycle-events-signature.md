---
created-on: 2024-01-31T16:23:08.517Z
f_long-description: >-
  ## Description
  

  In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.
  

  
  ### Before
  
  ```ts
  
  server.events.on('request:start', (req, reqId) => {
  	doStuff(req, reqId);
  });
  
  ```
  
  ### After
  
  ```ts
  
  server.events.on('request:start', ({ request, requestId }) => {
  	doStuff(request, requestId);
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/lifecycle-events-signature
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace lifecycle events callback signature [BETA]
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.517Z
published-on: 2024-01-31T16:23:08.517Z
seo:
  title: Registry Vcodemods - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  og:title: Registry Vcodemods - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace lifecycle events callback signature [BETA] | Codemod.com Automations
  description: In msw v2, lifecycle events callback methods have changed their signature
  twitter:card: In msw v2, lifecycle events callback methods have changed their signature
---
In msw v2, lifecycle events callback methods have changed their signature. This codemod replaces usages if its arguments with the new ones.