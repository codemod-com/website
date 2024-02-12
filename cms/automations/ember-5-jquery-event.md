---
created-on: 2024-02-12T11:28:08.762Z
f_long-description: >-
  ## Description
  

  Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod removes all calls to `originalEvent` in case of accessing properties that work with jQuery events as well as native events.
  

  
  ### Before:
  
  ```jsx
  
  // your event handler:
  export default Component.extend({
  	click(event) {
  		let x = event.originalEvent.clientX;
  	},
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  // your event handler:
  export default Component.extend({
  	click(event) {
  		let x = event.clientX;
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/jquery-event
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=8MIYv6K3Szow4WVYdgq1xyxfCT8
f_cli-command: codemod ember/5/jquery-event
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.3."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-jquery-event
title: Ember V5 - Jquery Event
f_slug-name: ember-5-jquery-event
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.762Z
published-on: 2024-02-12T11:28:08.762Z
seo:
  title: Ember V5 - Jquery Event | Codemod.com Automations
  og:title: Ember V5 - Jquery Event | Codemod.com Automations
  twitter:title: Ember V5 - Jquery Event | Codemod.com Automations
  description: Using event object APIs that are specific to jQuery
  twitter:card: Using event object APIs that are specific to jQuery
---
Using event object APIs that are specific to `jQuery.Event`, such as `originalEvent`, is deprecated in Ember.js v3.3. This codemod removes all calls to `originalEvent` in case of accessing properties that work with jQuery events as well as native events.