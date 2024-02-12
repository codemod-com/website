---
created-on: 2024-02-12T11:28:08.655Z
f_long-description: >-
  ## Description
  

  This codemod replaces all calls to `Ember.merge` with `Ember.assign`.
  

  
  ### Before:
  
  ```jsx
  
  import { merge } from '@ember/polyfills';
  
  var a = { first: 'Yehuda' };
  var b = { last: 'Katz' };
  merge(a, b);
  
  ```
  
  ### After:
  
  ```tsx
  
  import { assign } from '@ember/polyfills';
  
  var a = { first: 'Yehuda' };
  var b = { last: 'Katz' };
  assign(a, b);
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/deprecate-merge
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=SwH9ekSK1NDUt3QxSb3Hl4VfdAU
f_cli-command: codemod ember/5/deprecate-merge
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.6."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-deprecate-merge
title: Ember V5 - Deprecate Merge
f_slug-name: ember-5-deprecate-merge
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.655Z
published-on: 2024-02-12T11:28:08.655Z
seo:
  title: Ember V5 - Deprecate Merge | Codemod.com Automations
  og:title: Ember V5 - Deprecate Merge | Codemod.com Automations
  twitter:title: Ember V5 - Deprecate Merge | Codemod.com Automations
  description: This codemod replaces all calls to Ember
  twitter:card: This codemod replaces all calls to Ember
---
This codemod replaces all calls to `Ember.merge` with `Ember.assign`.