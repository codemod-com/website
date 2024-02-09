---
created-on: 2024-02-09T18:30:34.826Z
f_long-description: >-
  ## Description
  

  This codemod removes any usage of `new` with `A`, and calls `A` as a standard function.
  

  
  ### Before:
  
  ```jsx
  
  import { A } from '@ember/array';
  
  let arr = new A();
  
  ```
  
  ### After:
  
  ```tsx
  
  import { A as emberA } from '@ember/array';
  
  let arr = A();
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/array-wrapper
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=O6EOMpMfKAT8XBYI_9BmPbGjh2s
f_cli-command: codemod ember/5/array-wrapper
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.6."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-array-wrapper
title: Ember V5 - Array Wrapper
f_slug-name: ember-5-array-wrapper
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.826Z
published-on: 2024-02-09T18:30:34.826Z
seo:
  title: Ember V5 - Array Wrapper | Codemod.com Automations
  og:title: Ember V5 - Array Wrapper | Codemod.com Automations
  twitter:title: Ember V5 - Array Wrapper | Codemod.com Automations
  description: This codemod removes any usage of new` with `A`, and calls `A` as a standard function
  twitter:card: This codemod removes any usage of new` with `A`, and calls `A` as a standard function
---
This codemod removes any usage of `new` with `A`, and calls `A` as a standard function.