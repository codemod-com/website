---
created-on: 2024-02-09T18:30:34.884Z
f_long-description: >-
  ## Description
  

  This codemod transforms `get()` to `getProperties()` to use traditional object dot notation. This standard was proposed by Ember.js team in https://github.com/emberjs/rfcs/blob/master/text/0281-es5-getters.md.
  

  
  ### Before:
  
  ```jsx
  
  let chancancode = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  chancancode.get('fullName');
  
  let model = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  model.get('fullName');
  
  let route = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  route.get('fullName');
  
  let controller = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  controller.get('fullName');
  controller.get('foo.bar');
  controller.get('foo-bar');
  
  ```
  
  ### After:
  
  ```tsx
  
  let chancancode = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  chancancode.get('fullName');
  
  let model = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  model.get('fullName');
  
  let route = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  route.fullName;
  
  let controller = Person.create({ firstName: 'Godfrey', lastName: 'Chan' });
  
  controller.fullName;
  controller.get('foo.bar');
  controller['foo-bar'];
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/es5-getter-ember-codemod
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=gRfEFfyVMWOpWwejLmCFzbnPK8I
f_cli-command: codemod ember/5/es5-getter-ember-codemod
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.1."
f_verified-codemod: false
f_author: cms/authors/multiple-contributors.md
layout: "[automations].html"
slug: ember-5-es5-getter-ember-codemod
title: Ember V5 - ES5 Getter Ember Codemod
f_slug-name: ember-5-es5-getter-ember-codemod
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.884Z
published-on: 2024-02-09T18:30:34.884Z
seo:
  title: Ember V5 - ES5 Getter Ember Codemod | Codemod.com Automations
  og:title: Ember V5 - ES5 Getter Ember Codemod | Codemod.com Automations
  twitter:title: Ember V5 - ES5 Getter Ember Codemod | Codemod.com Automations
  description: This codemod transforms get()` to `getProperties()` to use traditional object dot notation
  twitter:card: This codemod transforms get()` to `getProperties()` to use traditional object dot notation
---
This codemod transforms `get()` to `getProperties()` to use traditional object dot notation. This standard was proposed by Ember.js team in https://github.com/emberjs/rfcs/blob/master/text/0281-es5-getters.md.