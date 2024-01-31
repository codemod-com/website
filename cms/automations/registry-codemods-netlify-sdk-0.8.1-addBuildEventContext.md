---
created-on: 2024-01-31T16:23:08.665Z
f_long-description: >-
  ## Description
  

  This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildContext(() => {});
  
  ```
  
  ### After
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildEventContext(() => {});
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/netlify-sdk/0.8.1/addBuildEventContext
f_framework: cms/framework/registry.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Rename addBuildEventContext
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.665Z
published-on: 2024-01-31T16:23:08.665Z
seo:
  title: Registry Vcodemods - Rename addBuildEventContext | Codemod.com Automations
  og:title: Registry Vcodemods - Rename addBuildEventContext | Codemod.com Automations
  twitter:title: Registry Vcodemods - Rename addBuildEventContext | Codemod.com Automations
  description: This codemod renames addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0
  twitter:card: This codemod renames addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0
---
This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.