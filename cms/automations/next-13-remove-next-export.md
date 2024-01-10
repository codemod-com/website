---
created-on: 2024-01-10T11:59:57.985Z
f_long-description: >-
  ## Description
  

  The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.
  

  
  ### Before (Shell files):
  
  ```sh
  
  npm run next build
  npm run next export
  
  ```
  
  ### After (Shell files):
  
  ```sh
  
  npm run next build
  
  ```
  
  ### Before (
  `next.config.js` files):
  
  ```javascript
  
  module.exports = {
  	distDir: 'out',
  };
  
  ```
  
  ### After (
  `next.config.js` files):
  
  ```javascript
  
  module.exports = {
  	distDir: 'out',
  	output: 'export',
  };
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/remove-next-export
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=GucjbUC1bYd_GLBT59TWiTGk2pY
f_cli-command: intuita next/13/remove-next-export
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version higher or equal to 13."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-remove-next-export
title: Next V13 - Remove Next Export
f_slug-name: next-13-remove-next-export
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.985Z
published-on: 2024-01-10T11:59:57.985Z
seo:
  title: Next V13 - Remove Next Export | Codemod.com Automations
  og:title: Next V13 - Remove Next Export | Codemod.com Automations
  twitter:title: Next V13 - Remove Next Export | Codemod.com Automations
  description: The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.
  twitter:card: The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.
---
The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.