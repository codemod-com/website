---
created-on: 2024-02-09T18:30:34.789Z
f_long-description: >-
  ## Description
  

  This codemod removes all calls to `willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener.
  

  
  ### Before:
  
  ```jsx
  
  import Router from '@ember/routing/router';
  import { inject as service } from '@ember/service';
  
  export default Router.extend({
  	currentUser: service('current-user'),
  
  	willTransition(transition) {
  		this._super(...arguments);
  		if (!this.currentUser.isLoggedIn) {
  			transition.abort();
  			this.transitionTo('login');
  		}
  	},
  
  	didTransition(privateInfos) {
  		this._super(...arguments);
  		ga.send('pageView', {
  			pageName: privateInfos.name,
  		});
  	},
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  import Router from '@ember/routing/router';
  import { inject as service } from '@ember/service';
  
  export default Router.extend({
  	currentUser: service('current-user'),
  
  	init() {
  		this._super(...arguments);
  
  		this.on('routeWillChange', (transition) => {
  			if (!this.currentUser.isLoggedIn) {
  				transition.abort();
  				this.transitionTo('login');
  			}
  		});
  
  		this.on('routeDidChange', (transition) => {
  			ga.send('pageView', {
  				pageName: privateInfos.name,
  			});
  		});
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/deprecate-router-events
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=mwdY99AT40pd8fQUil33BeR7SEo
f_cli-command: codemod ember/5/deprecate-router-events
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 3.6."
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: ember-5-deprecate-router-events
title: Ember V5 - Deprecate Router Events
f_slug-name: ember-5-deprecate-router-events
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.789Z
published-on: 2024-02-09T18:30:34.789Z
seo:
  title: Ember V5 - Deprecate Router Events | Codemod.com Automations
  og:title: Ember V5 - Deprecate Router Events | Codemod.com Automations
  twitter:title: Ember V5 - Deprecate Router Events | Codemod.com Automations
  description: This codemod removes all calls to willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener
  twitter:card: This codemod removes all calls to willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener
---
This codemod removes all calls to `willTransition` or `didTransition` events on the Router via usage of `routeWillChange` event listener and `routeDidChange` event listener.