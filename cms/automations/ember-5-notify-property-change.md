---
created-on: 2024-02-12T11:28:08.726Z
f_long-description: >-
  ## Description
  

  This codemod removes all calls to `propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange`.
  

  
  ### Before:
  
  ```jsx
  
  Ember.propertyWillChange(object, 'someProperty');
  doStuff(object);
  Ember.propertyDidChange(object, 'someProperty');
  
  object.propertyWillChange('someProperty');
  doStuff(object);
  object.propertyDidChange('someProperty');
  
  ```
  
  ### After:
  
  ```tsx
  
  doStuff(object);
  Ember.notifyPropertyChange(object, 'someProperty');
  
  doStuff(object);
  object.notifyPropertyChange('someProperty');
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/notify-property-change
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=TzYcFw0pbJTydA16tTFEvI3sM8M
f_cli-command: codemod ember/5/notify-property-change
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.1."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-notify-property-change
title: Ember V5 - Notify Property Change
f_slug-name: ember-5-notify-property-change
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.726Z
published-on: 2024-02-12T11:28:08.726Z
seo:
  title: Ember V5 - Notify Property Change | Codemod.com Automations
  og:title: Ember V5 - Notify Property Change | Codemod.com Automations
  twitter:title: Ember V5 - Notify Property Change | Codemod.com Automations
  description: This codemod removes all calls to propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange
  twitter:card: This codemod removes all calls to propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange
---
This codemod removes all calls to `propertyWillChange` and replaces all calls to `propertyDidChange` with `notifyPropertyChange`.