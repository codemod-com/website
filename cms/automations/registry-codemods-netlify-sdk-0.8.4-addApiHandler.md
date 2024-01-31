---
created-on: 2024-01-31T16:23:08.763Z
f_long-description: >-
  ## Description
  

  This codemod renames `addHandler` to `addApiHandler` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  integration.addHandler('some-function', async (event, context) => {});
  
  ```
  
  ### After
  
  ```jsx
  
  import { NetlifyIntegration } from '@netlify/sdk';
  
  const integration = new NetlifyIntegration();
  
  integration.addApiHandler('some-function', async (event, context) => {});
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/netlify-sdk/0.8.4/addApiHandler
f_framework: cms/framework/registry.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - addApiHandler
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.763Z
published-on: 2024-01-31T16:23:08.763Z
seo:
  title: Registry Vcodemods - addApiHandler | Codemod.com Automations
  og:title: Registry Vcodemods - addApiHandler | Codemod.com Automations
  twitter:title: Registry Vcodemods - addApiHandler | Codemod.com Automations
  description: This codemod renames addHandler` to `addApiHandler` as required in Netlify SDK v0
  twitter:card: This codemod renames addHandler` to `addApiHandler` as required in Netlify SDK v0
---
This codemod renames `addHandler` to `addApiHandler` as required in Netlify SDK v0.8.1.