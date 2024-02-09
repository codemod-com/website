---
created-on: 2024-02-09T18:30:34.754Z
f_long-description: >-
  ## Description
  

  `new EmberObject()` is deprecated in Ember.js v3.9 in favor of constructing instances of `EmberObject` and its subclasses. This codemod replaces all calls to `new EmberObject()` with `EmberObject.create()` and adds a `constructor` function to classes that extend from `EmberObject` so that the classes no longer extend from `EmberObject`.
  

  
  ### Before:
  
  ```jsx
  
  let obj1 = new EmberObject();
  let obj2 = new EmberObject({ prop: 'value' });
  
  const Foo = EmberObject.extend();
  let foo = new Foo({ bar: 123 });
  
  ```
  
  ### After:
  
  ```tsx
  
  let obj1 = EmberObject.create();
  let obj2 = EmberObject.create({ prop: 'value' });
  
  const Foo = EmberObject.extend();
  let foo = new Foo({ bar: 123 });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/object-new-constructor
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=DByr5sk2809c2rfO8_TvT-RB0Pw
f_cli-command: codemod ember/5/object-new-constructor
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.6."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-object-new-constructor
title: Ember V5 - Object New Constructor
f_slug-name: ember-5-object-new-constructor
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.754Z
published-on: 2024-02-09T18:30:34.754Z
seo:
  title: Ember V5 - Object New Constructor | Codemod.com Automations
  og:title: Ember V5 - Object New Constructor | Codemod.com Automations
  twitter:title: Ember V5 - Object New Constructor | Codemod.com Automations
  description: new EmberObject()` is deprecated in Ember
  twitter:card: new EmberObject()` is deprecated in Ember
---
`new EmberObject()` is deprecated in Ember.js v3.9 in favor of constructing instances of `EmberObject` and its subclasses. This codemod replaces all calls to `new EmberObject()` with `EmberObject.create()` and adds a `constructor` function to classes that extend from `EmberObject` so that the classes no longer extend from `EmberObject`.