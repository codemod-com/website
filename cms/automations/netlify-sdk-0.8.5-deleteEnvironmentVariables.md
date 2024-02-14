---
created-on: 2024-01-10T11:59:57.757Z
f_long-description: >-
  ## Description
  

  This codemod changes `deleteEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```JavaScript
  
  deleteEnvironmentVariables(accountId, siteId, variables);
  
  ```
  
  ### After
  
  ```JavaScript
  
  deleteEnvironmentVariables({
  	accountId: accountId,
  	siteId: siteId,
  	variables: variables,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/deleteEnvironmentVariables
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=XItqcs3BFmoc9QE_2xBK0kVcpE0
f_cli-command: codemod netlify/0.8.5/deleteEnvironmentVariables
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.5-deleteEnvironmentVariables
title: Netlify-sdk V0.8.5 - deleteEnvironmentVariables
f_slug-name: netlify-0.8.5-deleteEnvironmentVariables
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.757Z
published-on: 2024-01-10T11:59:57.757Z
seo:
  title: Netlify-sdk V0.8.5 - deleteEnvironmentVariables
  description: This codemod changes `deleteEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `deleteEnvironmentVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.