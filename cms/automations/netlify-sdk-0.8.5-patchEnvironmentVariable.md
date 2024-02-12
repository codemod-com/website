---
created-on: 2024-01-10T11:59:57.820Z
f_long-description: >-
  ## Description
  

  This codemod changes `patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
  

  
  ### Before
  
  ```JavaScript
  
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
  
  ```JavaScript
  
  patchEnvironmentVariable({
  	accountId: accountId,
  	siteId: siteId,
  	key: key,
  	context: context,
  	value: value,
  	contextParameter: contextParameter,
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.5/patchEnvironmentVariable
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=GHm-VFIY-Pxm4LAGz0KjuPAJ_ss
f_cli-command: intuita netlify/0.8.5/patchEnvironmentVariable
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.5 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.5-patchEnvironmentVariable
title: Netlify-sdk V0.8.5 - patchEnvironmentVariable
f_slug-name: netlify-0.8.5-patchEnvironmentVariable
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.820Z
published-on: 2024-01-10T11:59:57.820Z
seo:
  title: Netlify-sdk V0.8.5 - patchEnvironmentVariable
  description: This codemod changes `patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.
---
This codemod changes `patchEnvironmentVariable` to pass an object instead of the separate arguments as required in Netlify SDK v0.8.5.