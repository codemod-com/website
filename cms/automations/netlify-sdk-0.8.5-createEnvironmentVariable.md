---
created-on: 2024-01-10T11:59:57.682Z
f_long-description: >-
  ## Description
  

  This codemod changes `createEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```jsx
  
  createEnvironmentVariable(accountId, siteId, key, values);
  
  ```
  
  ### After
  
  ```jsx
  
  createEnvironmentVariable({
  	accountId: accountId,
  	siteId: siteId,
  	key: key,
  	values: values,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/createEnvironmentVariable
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=IcK_ayBC2DCMuu9Klhwolg-ZiOc
f_cli-command: intuita netlify/0.8.5/createEnvironmentVariable
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: netlify-0.8.5-createEnvironmentVariable
title: Netlify-sdk V0.8.5 - createEnvironmentVariable
f_slug-name: netlify-0.8.5-createEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.682Z
published-on: 2024-01-10T11:59:57.682Z
seo:
  title: Netlify-sdk V0.8.5 - createEnvironmentVariable | Codemod.com Automations
  og:title: Netlify-sdk V0.8.5 - createEnvironmentVariable | Codemod.com Automations
  twitter:title: Netlify-sdk V0.8.5 - createEnvironmentVariable | Codemod.com Automations
  description: This codemod changes `createEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  twitter:card: This codemod changes `createEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `createEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.