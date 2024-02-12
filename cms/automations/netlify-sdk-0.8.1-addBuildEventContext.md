---
created-on: 2024-01-10T11:59:57.583Z
f_long-description: >-
  ## Description
  

  This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```JavaScript
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildContext(() => {});
  
  ```
  
  ### After
  
  ```JavaScript
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildEventContext(() => {});
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.1/addBuildEventContext
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=B4dvpPVS0er2UmYuLj_idGSFfng
f_cli-command: intuita netlify/0.8.1/addBuildEventContext
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.1-addBuildEventContext
title: Netlify-sdk V0.8.1 - Rename addBuildEventContext
f_slug-name: netlify-0.8.1-addBuildEventContext
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.583Z
published-on: 2024-01-10T11:59:57.583Z
seo:
  title: Netlify-sdk V0.8.1 - Rename addBuildEventContext
  og:title: Netlify-sdk V0.8.1 - Rename addBuildEventContext
  twitter:title: Netlify-sdk V0.8.1 - Rename addBuildEventContext
  description: This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.
  twitter:card: This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.
---
This codemod renames `addBuildContext` to `addBuildEventContext` as required in Netlify SDK v0.8.1.