---
created-on: 2024-01-10T11:59:57.844Z
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
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/updateEnvironmentVariable
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=cre47t7HZY7d1I3PIOIEnG4jgcg
f_cli-command: intuita netlify/0.8.5/updateEnvironmentVariable
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: netlify-0.8.5-updateEnvironmentVariable
title: Netlify-sdk V0.8.5 - updateEnvironmentVariable
f_slug-name: netlify-0.8.5-updateEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.844Z
published-on: 2024-01-10T11:59:57.844Z
seo:
  title: Netlify-sdk V0.8.5 - updateEnvironmentVariable | Codemod.com Automations
  og:title: Netlify-sdk V0.8.5 - updateEnvironmentVariable | Codemod.com Automations
  twitter:title: Netlify-sdk V0.8.5 - updateEnvironmentVariable | Codemod.com Automations
  description: This codemod changes `updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  twitter:card: This codemod changes `updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `updateEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.