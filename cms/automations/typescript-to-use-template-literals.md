---
created-on: 2024-02-12T11:28:07.948Z
f_long-description: >-
  ## Description
  

  This codemod replaces string concatenations with template literals.
  

  
  ### Before
  
  ```JavaScript
  
  const name = 'John';
  const greeting = 'Hello, ' + name + '!';
  
  ```
  
  ### After
  
  ```JavaScript
  
  const name = 'John';
  const greeting = `Hello, ${name}!`;
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/typescript/use-template-literals
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=_za2QFnY7eFaBvBfvuwb_vin7xM
f_cli-command: codemod typescript/use-template-literals
f_framework: cms/framework/typescript.md
f_applicability-criteria: "TypeScript version higher or equal to 1.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: typescript-use-template-literals
title: Typescript to use-template-literals - Use Template Literals
f_slug-name: typescript-use-template-literals
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~2 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:07.948Z
published-on: 2024-02-12T11:28:07.948Z
seo:
  title: Typescript to use-template-literals - Use Template Literals
  description: This codemod replaces string concatenations with template literals
---
This codemod replaces string concatenations with template literals.