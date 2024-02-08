---
created-on: 2024-01-10T11:59:57.615Z
f_long-description: >-
  ## Description
  

  This codemod renames `disableBuildhook` to `disableBuildEventHandlers` as required in Netlify SDK v0.8.1.
  

  
  ### Before
  
  ```jsx
  
  await client.disableBuildhook(siteId);
  
  ```
  
  ### After
  
  ```jsx
  
  await client.disableBuildEventHandlers(siteId);
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/netlify-sdk/0.8.1/disableBuildEventHandlers
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=w6jKvC5ucc2ZSdO5xFabXo_nEYc
f_cli-command: intuita netlify/0.8.1/disableBuildEventHandlers
f_framework: cms/framework/netlify-sdk.md
f_applicability-criteria: "Netlify SDK v0.8.1 or higher."
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: netlify-0.8.1-disableBuildEventHandlers
title: Netlify-sdk V0.8.1 - Rename disableBuildEventHandlers
f_slug-name: netlify-0.8.1-disableBuildEventHandlers
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.615Z
published-on: 2024-01-10T11:59:57.615Z
seo:
  title: Netlify-sdk V0.8.1 - Rename disableBuildEventHandlers | Codemod.com Automations
  og:title: Netlify-sdk V0.8.1 - Rename disableBuildEventHandlers | Codemod.com Automations
  twitter:title: Netlify-sdk V0.8.1 - Rename disableBuildEventHandlers | Codemod.com Automations
  description: This codemod renames `disableBuildhook` to `disableBuildEventHandlers` as required in Netlify SDK v0.8.1.
  twitter:card: This codemod renames `disableBuildhook` to `disableBuildEventHandlers` as required in Netlify SDK v0.8.1.
---
This codemod renames `disableBuildhook` to `disableBuildEventHandlers` as required in Netlify SDK v0.8.1.