---
created-on: 2024-02-12T11:28:07.962Z
f_long-description: >-
  ## Description
  

  This codemod removes public modifier in interface declarations as it is implicit.
  

  
  ### Before
  
  ```JavaScript
  
  class MyClass {
      public myProperty: string;
  
      public constructor() {
      }
  
      public myMethod(): void {
      }
  }
  
  ```
  
  ### After
  
  ```JavaScript
  
  class MyClass {
      myProperty: string;
  
      constructor() {
      }
  
      myMethod(): void {
      }
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/typescript/remove-public-modifier
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=OqFg7teIegbJUKc1o_pWxGcdfGM
f_cli-command: codemod typescript/remove-public-modifier
f_framework: cms/framework/typescript.md
f_applicability-criteria: "TypeScript version higher or equal to 1.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: typescript-remove-public-modifier
title: Typescript to remove-public-modifier - Remove Public Modifier
f_slug-name: typescript-remove-public-modifier
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minute/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:07.962Z
published-on: 2024-02-12T11:28:07.962Z
seo:
  title: Typescript to remove-public-modifier - Remove Public Modifier
  og:title: Typescript to remove-public-modifier - Remove Public Modifier
  twitter:title: Typescript to remove-public-modifier - Remove Public Modifier
  description: This codemod removes public modifier in interface declarations as it is implicit
  twitter:card: This codemod removes public modifier in interface declarations as it is implicit
---
This codemod removes public modifier in interface declarations as it is implicit.