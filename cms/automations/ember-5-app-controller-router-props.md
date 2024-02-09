---
created-on: 2024-02-09T18:30:34.908Z
f_long-description: >-
  ## Description
  

  This codemod replaces all occurrences of `this.currentRouteName` with `this.router.currentRouteName`
  and `this.currentPath` with `this.router.currentPath`.
  

  
  ### Before:
  
  ```jsx
  
  import Controller from '@ember/controller';
  import fetch from 'fetch';
  
  export default Controller.extend({
  	store: service('store'),
  
  	actions: {
  		sendPayload() {
  			fetch('/endpoint', {
  				method: 'POST',
  				body: JSON.stringify({
  					route: this.currentRouteName,
  				}),
  			});
  		},
  	},
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  import Controller from '@ember/controller';
  import fetch from 'fetch';
  
  export default Controller.extend({
  	router: service('router'),
  	store: service('store'),
  
  	actions: {
  		sendPayload() {
  			fetch('/endpoint', {
  				method: 'POST',
  				body: JSON.stringify({
  					route: this.router.currentRouteName,
  				}),
  			});
  		},
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/app-controller-router-props
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=2ilOsMOt-d18XxYxfiO3RhiKtOI
f_cli-command: codemod ember/5/app-controller-router-props
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.10."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-app-controller-router-props
title: Ember V5 - App Controller Router Props
f_slug-name: ember-5-app-controller-router-props
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.908Z
published-on: 2024-02-09T18:30:34.908Z
seo:
  title: Ember V5 - App Controller Router Props | Codemod.com Automations
  og:title: Ember V5 - App Controller Router Props | Codemod.com Automations
  twitter:title: Ember V5 - App Controller Router Props | Codemod.com Automations
  description: This codemod replaces all occurrences of this
  twitter:card: This codemod replaces all occurrences of this
---
This codemod replaces all occurrences of `this.currentRouteName` with `this.router.currentRouteName`