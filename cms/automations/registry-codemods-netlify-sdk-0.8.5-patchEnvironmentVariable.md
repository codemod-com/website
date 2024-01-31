---
created-on: 2024-01-31T16:23:08.918Z
f_long-description: >-
  ## Description
  

  This codemod changes `patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```jsx
  
  patchEnvironmentVariable(
  	accountId,
  	siteId,
  	key,
  	context,
  	value,
  	contextParameter,
  );
  
  ```
  
  ### After
  
  ```jsx
  
  patchEnvironmentVariable({
  	accountId: accountId,
  	siteId: siteId,
  	key: key,
  	context: context,
  	value: value,
  	contextParameter: contextParameter,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/netlify-sdk/0.8.5/patchEnvironmentVariable
f_framework: cms/framework/registry.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - patchEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.918Z
published-on: 2024-01-31T16:23:08.918Z
seo:
  title: Registry Vcodemods - patchEnvironmentVariable | Codemod.com Automations
  og:title: Registry Vcodemods - patchEnvironmentVariable | Codemod.com Automations
  twitter:title: Registry Vcodemods - patchEnvironmentVariable | Codemod.com Automations
  description: This codemod changes patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0
  twitter:card: This codemod changes patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0
---
This codemod changes `patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.