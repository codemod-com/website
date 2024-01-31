---
created-on: 2024-01-31T16:23:08.405Z
f_long-description: >-
  ## Description
  

  Run this codemod to upgrade your codebase from using mocha to vitest.
  

  
  ### Before
  
  ```ts
  
  import { expect } from 'chai';
  
  describe('Test Suite 1', () => {
  	it('addition', () => {
  		expect(1 + 1).to.equal(2);
  	});
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { describe, expect, it } from 'vitest';
  
  describe('Test Suite 1', () => {
  	it('addition', () => {
  		expect(1 + 1).to.equal(2);
  	});
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/mocha/vitest/migrate-tests
f_framework: cms/framework/registry.md
f_applicability-criteria: "`mocha` >= 9.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Migrate Tests from Mocha to Vitest
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5+ minutes/file"
tags: automations
updated-on: 2024-01-31T16:23:08.405Z
published-on: 2024-01-31T16:23:08.405Z
seo:
  title: Registry Vcodemods - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  og:title: Registry Vcodemods - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  twitter:title: Registry Vcodemods - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  description: Run this codemod to upgrade your codebase from using mocha to vitest
  twitter:card: Run this codemod to upgrade your codebase from using mocha to vitest
---
Run this codemod to upgrade your codebase from using mocha to vitest.