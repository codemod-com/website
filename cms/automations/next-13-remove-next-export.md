---
created-on: 2023-11-30T16:54:10.586Z
f_long-description: >-
  ## Description


  The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.


  ## Example


  ### Before (Shell files):


  ```shell

  npm run next build

  npm run next export

  ```


  ### After (Shell files):


  ```shell

  npm run next build

  ```


  ### Before (`next.config.js` files):


  ```javascript

  module.exports = {
  	distDir: 'out',
  };

  ```


  ### After (`next.config.js` files):


  ```javascript

  module.exports = {
  	distDir: 'out',
  	output: 'export',
  };

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/blob/main/codemods/next/13/remove-next-export
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=GucjbUC1bYd_GLBT59TWiTGk2pY
f_cli-command: intuita next/13/remove-next-export
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version higher or equal to 13.
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Remove Next Export
updated-on: 2023-11-30T16:54:10.597Z
published-on: 2023-11-30T16:54:10.610Z
f_slug-name: remove-next-export
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T16:54:10.618Z
seo:
  title: Next.js Remove Next Export | Codemod.com
  description: This automation dangerously removes all references to the command in
    `*.md`, `*.sh`, `package.json`.
---
This automation dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`.