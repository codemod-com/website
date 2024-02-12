---
created-on: 2024-02-12T11:28:08.690Z
f_long-description: >-
  ## Description
  

  `.property()` is a modifier that adds additional property dependencies to an existing computed property. This codemod moves the dependencies to the main computed property definition.
  

  
  ### Before:
  
  ```jsx
  
  const Person = EmberObject.extend({
  	fullName: computed(function () {
  		return `${this.firstName} ${this.lastName}`;
  	}).property('firstName', 'lastName'),
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  const Person = EmberObject.extend({
  	fullName: computed('firstName', 'lastName', function () {
  		return `${this.firstName} ${this.lastName}`;
  	}),
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/cp-property
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=UEjLA-WkII1TJWdF-uBUDh_EGtk
f_cli-command: codemod ember/5/cp-property
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.9."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-cp-property
title: Ember V5 - Cp Property
f_slug-name: ember-5-cp-property
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.690Z
published-on: 2024-02-12T11:28:08.690Z
seo:
  title: Ember V5 - Cp Property | Codemod.com Automations
  og:title: Ember V5 - Cp Property | Codemod.com Automations
  twitter:title: Ember V5 - Cp Property | Codemod.com Automations
  description: 
  twitter:card:
---
`.property()` is a modifier that adds additional property dependencies to an existing computed property. This codemod moves the dependencies to the main computed property definition.