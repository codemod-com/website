---
created-on: 2024-01-31T16:23:08.935Z
f_long-description: >-
  ## Description
  

  This codemod changes `updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```jsx
  
  updateEnvironmentVariable(accountId, siteId, key, values);
  
  ```
  
  ### After
  
  ```jsx
  
  updateEnvironmentVariable({
  	accountId: accountId,
  	siteId: siteId,
  	key: key,
  	values: values,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/netlify-sdk/0.8.5/updateEnvironmentVariable
f_framework: cms/framework/registry.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - updateEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.935Z
published-on: 2024-01-31T16:23:08.935Z
seo:
  title: Registry Vcodemods - updateEnvironmentVariable | Codemod.com Automations
  og:title: Registry Vcodemods - updateEnvironmentVariable | Codemod.com Automations
  twitter:title: Registry Vcodemods - updateEnvironmentVariable | Codemod.com Automations
  description: This codemod changes updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0
  twitter:card: This codemod changes updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0
---
This codemod changes `updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.