---
created-on: 2024-01-10T11:59:57.776Z
f_long-description: >-
  ## Description
  

  This codemod changes `getEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```JavaScript
  
  getEnvironmentVariables(accountId, siteId);
  
  ```
  
  ### After
  
  ```JavaScript
  
  getEnvironmentVariables({
  	accountId: accountId,
  	siteId: siteId,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/getEnvironmentVariables
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=ukodvFWnCAHJXxg3LtnMKKjGt6I
f_cli-command: codemod netlify/0.8.5/getEnvironmentVariables
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.5-getEnvironmentVariables
title: Netlify-sdk V0.8.5 - getEnvironmentVariables
f_slug-name: netlify-0.8.5-getEnvironmentVariables
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.776Z
published-on: 2024-01-10T11:59:57.776Z
seo:
  title: Netlify-sdk V0.8.5 - getEnvironmentVariables
  description: This codemod changes `getEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `getEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.