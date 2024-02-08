---
created-on: 2024-01-10T11:59:57.599Z
f_long-description: >-
  ## Description
  

  This codemod renames `addBuildHook` to `addBuildEventHandler` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildHook('onPreBuild', () => {
  	console.log('This is my first build event handler!');
  });
  
  ```
  
  ### After
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  // Adding a build event handler
  integration.addBuildEventHandler('onPreBuild', () => {
  	console.log('This is my first build event handler!');
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.1/addBuildEventHandler
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=sOl2zy2FQYSHKink4a0XI_l8-3E
f_cli-command: intuita netlify/0.8.1/addBuildEventHandler
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.1-addBuildEventHandler
title: Netlify-sdk V0.8.1 - Rename addBuildEventHandler
f_slug-name: netlify-0.8.1-addBuildEventHandler
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.599Z
published-on: 2024-01-10T11:59:57.599Z
seo:
  title: Netlify-sdk V0.8.1 - Rename addBuildEventHandler | Codemod.com Automations
  og:title: Netlify-sdk V0.8.1 - Rename addBuildEventHandler | Codemod.com Automations
  twitter:title: Netlify-sdk V0.8.1 - Rename addBuildEventHandler | Codemod.com Automations
  description: This codemod renames `addBuildHook` to `addBuildEventHandler` as required in Netlify SDK v0.8.1.
  twitter:card: This codemod renames `addBuildHook` to `addBuildEventHandler` as required in Netlify SDK v0.8.1.
---
This codemod renames `addBuildHook` to `addBuildEventHandler` as required in Netlify SDK v0.8.1.