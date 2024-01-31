---
created-on: 2024-01-31T16:23:09.085Z
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
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/remove-next-export
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version higher or equal to 13."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Remove Next Export
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:09.085Z
published-on: 2024-01-31T16:23:09.085Z
seo:
  title: Registry Vcodemods - Remove Next Export | Codemod.com Automations
  og:title: Registry Vcodemods - Remove Next Export | Codemod.com Automations
  twitter:title: Registry Vcodemods - Remove Next Export | Codemod.com Automations
  description: The next export` command is deprecated
  twitter:card: The next export` command is deprecated
---
The `next export` command is deprecated. This codemod dangerously removes all references to the command in `*.md`, `*.sh`, `package.json`. It also adds a property `output` with the value `export` to the `module.exports` object in `next.config.js` files.