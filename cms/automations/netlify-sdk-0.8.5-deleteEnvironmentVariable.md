---
created-on: 2024-01-10T11:59:57.737Z
f_long-description: >-
  ## Description
  

  This codemod changes `deleteEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```JavaScript
  
  deleteEnvironmentVariable(accountId, siteId, key);
  
  ```
  
  ### After
  
  ```JavaScript
  
  deleteEnvironmentVariable({
  	accountId: accountId,
  	siteId: siteId,
  	key: key,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/deleteEnvironmentVariable
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=zYg4oVcYTrFgw_M1m0ok8PQxvqE
f_cli-command: intuita netlify/0.8.5/deleteEnvironmentVariable
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.5-deleteEnvironmentVariable
title: Netlify-sdk V0.8.5 - deleteEnvironmentVariable
f_slug-name: netlify-0.8.5-deleteEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.737Z
published-on: 2024-01-10T11:59:57.737Z
seo:
  title: Netlify-sdk V0.8.5 - deleteEnvironmentVariable
  og:title: Netlify-sdk V0.8.5 - deleteEnvironmentVariable
  twitter:title: Netlify-sdk V0.8.5 - deleteEnvironmentVariable
  description: This codemod changes `deleteEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  twitter:card: This codemod changes `deleteEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `deleteEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.