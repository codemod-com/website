---
created-on: 2024-01-10T11:59:57.665Z
f_long-description: >-
  ## Description
  

  This codemod renames `addHandler` to `addApiHandler` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```JavaScript
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  integration.addHandler('some-function', async (event, context) => {});
  
  ```
  
  ### After
  
  ```JavaScript
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  integration.addApiHandler('some-function', async (event, context) => {});
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.4/addApiHandler
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=mDhW-pAC6YyLv6EtqGUILgH-Wwc
f_cli-command: intuita netlify/0.8.4/addApiHandler
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.4-addApiHandler
title: Netlify-sdk V0.8.4 - addApiHandler
f_slug-name: netlify-0.8.4-addApiHandler
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.665Z
published-on: 2024-01-10T11:59:57.665Z
seo:
  title: Netlify-sdk V0.8.4 - addApiHandler
  description: This codemod renames `addHandler` to `addApiHandler` as required in Netlify SDK v0.8.1.
---
This codemod renames `addHandler` to `addApiHandler` as required in Netlify SDK v0.8.1.