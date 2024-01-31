---
created-on: 2024-01-31T16:23:08.820Z
f_long-description: >-
  ## Description
  

  This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```jsx
  
  createOrUpdateVariables(accountId, siteId, variables);
  
  ```
  
  ### After
  
  ```jsx
  
  createOrUpdateVariables({
  	accountId: accountId,
  	siteId: siteId,
  	key: variables,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/netlify-sdk/0.8.5/createOrUpdateVariables
f_framework: cms/framework/registry.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - createOrUpdateVariables
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.820Z
published-on: 2024-01-31T16:23:08.820Z
seo:
  title: Registry Vcodemods - createOrUpdateVariables | Codemod.com Automations
  og:title: Registry Vcodemods - createOrUpdateVariables | Codemod.com Automations
  twitter:title: Registry Vcodemods - createOrUpdateVariables | Codemod.com Automations
  description: This codemod changes createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0
  twitter:card: This codemod changes createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0
---
This codemod changes `createOrUpdateVariables` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.