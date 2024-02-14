---
created-on: 2024-01-10T11:59:57.632Z
f_long-description: >-
  ## Description
  

  This codemod renames `enableBuildhook` to `enableBuildEventHandlers` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```JavaScript
  
  await client.enableBuildhook(siteId);
  
  ```
  
  ### After
  
  ```JavaScript
  
  await client.enableBuildEventHandlers(siteId);
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.1/enableBuildEventHandlers
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=NNDeo-DrkLwZArLN0RoY9c-0wjA
f_cli-command: codemod netlify/0.8.1/enableBuildEventHandlers
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.1-enableBuildEventHandlers
title: Netlify-sdk V0.8.1 - Rename enableBuildEventHandlers
f_slug-name: netlify-0.8.1-enableBuildEventHandlers
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.632Z
published-on: 2024-01-10T11:59:57.632Z
seo:
  title: Netlify-sdk V0.8.1 - Rename enableBuildEventHandlers
  description: This codemod renames `enableBuildhook` to `enableBuildEventHandlers` as required in Netlify SDK v0.8.1.
---
This codemod renames `enableBuildhook` to `enableBuildEventHandlers` as required in Netlify SDK v0.8.1.