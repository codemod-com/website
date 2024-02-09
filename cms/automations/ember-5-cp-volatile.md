---
created-on: 2024-02-09T18:30:34.743Z
f_long-description: >-
  ## Description
  

  This codemod removes all calls to `volatile()` and ensures that native getters are directly used.
  

  
  ### Before:
  
  ```jsx
  
  const Person = EmberObject.extend({
  	fullName: computed(function () {
  		return `${this.firstName} ${this.lastName}`;
  	}).volatile(),
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  const Person = EmberObject.extend({
  	get fullName() {
  		return `${this.firstName} ${this.lastName}`;
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/cp-volatile
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=t0qpljVDAowX4w-aSSghMAMIa38
f_cli-command: codemod ember/5/cp-volatile
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.9."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-cp-volatile
title: Ember V5 - Cp Volatile
f_slug-name: ember-5-cp-volatile
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.743Z
published-on: 2024-02-09T18:30:34.743Z
seo:
  title: Ember V5 - Cp Volatile | Codemod.com Automations
  og:title: Ember V5 - Cp Volatile | Codemod.com Automations
  twitter:title: Ember V5 - Cp Volatile | Codemod.com Automations
  description: This codemod removes all calls to volatile()` and ensures that native getters are directly used
  twitter:card: This codemod removes all calls to volatile()` and ensures that native getters are directly used
---
This codemod removes all calls to `volatile()` and ensures that native getters are directly used.