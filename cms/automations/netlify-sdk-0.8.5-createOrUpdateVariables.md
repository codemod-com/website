---
created-on: 2024-01-10T11:59:57.714Z
f_long-description: >-
  ## Description
  

  This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```JavaScript
  
  createOrUpdateVariables(accountId, siteId, variables);
  
  ```
  
  ### After
  
  ```TypeScript
  
  createOrUpdateVariables({
  	accountId: accountId,
  	siteId: siteId,
  	key: variables,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/createOrUpdateVariables
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=JYPkh5WUe3gjYCsvlXJDVQUSFMw
f_cli-command: intuita netlify/0.8.5/createOrUpdateVariables
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.5-createOrUpdateVariables
title: Netlify-sdk V0.8.5 - createOrUpdateVariables
f_slug-name: netlify-0.8.5-createOrUpdateVariables
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.714Z
published-on: 2024-01-10T11:59:57.714Z
seo:
  title: Netlify-sdk V0.8.5 - createOrUpdateVariables | Codemod.com Automations
  og:title: Netlify-sdk V0.8.5 - createOrUpdateVariables | Codemod.com Automations
  twitter:title: Netlify-sdk V0.8.5 - createOrUpdateVariables | Codemod.com Automations
  description: This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  twitter:card: This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.