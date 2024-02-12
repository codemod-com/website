---
created-on: 2024-02-12T11:28:08.702Z
f_long-description: >-
  ## Description
  

  Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod ensures the access to the native event without triggering any deprecations via wrapping the `event` with the `normalizeEvent` function provided by `ember-jquery-legacy`.
  

  
  ### Before:
  
  ```jsx
  
  export default Component.extend({
  	click(event) {
  		let nativeEvent = event.originalEvent;
  	},
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  import { normalizeEvent } from 'ember-jquery-legacy';
  
  export default Component.extend({
  	click(event) {
  		let nativeEvent = normalizeEvent(event);
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/ember-jquery-legacy
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=7ov34iPxeWaG6gKTD3mLR4ksgM0
f_cli-command: codemod ember/5/ember-jquery-legacy
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.3."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-ember-jquery-legacy
title: Ember V5 - Ember Jquery Legacy
f_slug-name: ember-5-ember-jquery-legacy
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.702Z
published-on: 2024-02-12T11:28:08.702Z
seo:
  title: Ember V5 - Ember Jquery Legacy | Codemod.com Automations
  og:title: Ember V5 - Ember Jquery Legacy | Codemod.com Automations
  twitter:title: Ember V5 - Ember Jquery Legacy | Codemod.com Automations
  description: Using event object APIs that are specific to jQuery
  twitter:card: Using event object APIs that are specific to jQuery
---
Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod ensures the access to the native event without triggering any deprecations via wrapping the `event` with the `normalizeEvent` function provided by `ember-jquery-legacy`.