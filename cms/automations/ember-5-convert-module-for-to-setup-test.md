---
created-on: 2024-02-12T11:28:08.667Z
f_long-description: >-
  ## Description
  

  This codemod transforms from the older `moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax.
  

  
  ### Before:
  
  ```tsx
  
  import { moduleFor, test } from 'ember-qunit';
  
  moduleFor('service:flash', 'Unit | Service | Flash', {
  	unit: true,
  });
  
  test('should allow messages to be queued', function (assert) {
  	let subject = this.subject();
  });
  
  ```
  
  ### After:
  
  ```tsx
  
  import { setupTest } from 'ember-qunit';
  import { module, test } from 'qunit';
  
  module('Unit | Service | Flash', function (hooks) {
  	setupTest(hooks);
  
  	test('should allow messages to be queued', function (assert) {
  		let subject = this.owner.lookup('service:flash');
  	});
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/ember/5/convert-module-for-to-setup-test
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=VTupulWTlhXH3W_vzfSGItBnJM4
f_cli-command: codemod ember/5/convert-module-for-to-setup-test
f_framework: cms/framework/ember.md
f_applicability-criteria: "Ember.js version higher or equal to 2.4."
f_verified-codemod: false
f_author: cms/authors/robert-jackson.md
layout: "[automations].html"
slug: ember-5-convert-module-for-to-setup-test
title: Ember V5 - Convert moduleFor to setupTest
f_slug-name: ember-5-convert-module-for-to-setup-test
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.667Z
published-on: 2024-02-12T11:28:08.667Z
seo:
  title: Ember V5 - Convert moduleFor to setupTest | Codemod.com Automations
  og:title: Ember V5 - Convert moduleFor to setupTest | Codemod.com Automations
  twitter:title: Ember V5 - Convert moduleFor to setupTest | Codemod.com Automations
  description: This codemod transforms from the older moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax
  twitter:card: This codemod transforms from the older moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax
---
This codemod transforms from the older `moduleFor*` syntax of `ember-qunit@2` to the newer `setup*Test` syntax.