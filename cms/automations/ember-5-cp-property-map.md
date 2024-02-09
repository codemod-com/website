---
created-on: 2024-02-09T18:30:34.896Z
f_long-description: >-
  ## Description
  

  `.property()` is a modifier that adds additional property dependencies to an existing computed property. For `filter`, `map`, and `sort` computed property macros, this codemod ensures they receive an array of additional dependent keys as a second parameter.
  

  
  ### Before:
  
  ```jsx
  
  const Person = EmberObject.extend({
  	friendNames: map('friends', function (friend) {
  		return friend[this.get('nameKey')];
  	}).property('nameKey'),
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  const Person = EmberObject.extend({
  	friendNames: map('friends', ['nameKey'], function (friend) {
  		return friend[this.get('nameKey')];
  	}),
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/cp-property-map
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=T2qg3WOT4qOdTHg0LnDcfh16j30
f_cli-command: codemod ember/5/cp-property-map
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.9."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-cp-property-map
title: Ember V5 - Cp Property Map
f_slug-name: ember-5-cp-property-map
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.896Z
published-on: 2024-02-09T18:30:34.896Z
seo:
  title: Ember V5 - Cp Property Map | Codemod.com Automations
  og:title: Ember V5 - Cp Property Map | Codemod.com Automations
  twitter:title: Ember V5 - Cp Property Map | Codemod.com Automations
  description: 
  twitter:card:
---
`.property()` is a modifier that adds additional property dependencies to an existing computed property. For `filter`, `map`, and `sort` computed property macros, this codemod ensures they receive an array of additional dependent keys as a second parameter.