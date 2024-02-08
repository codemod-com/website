---
created-on: 2024-01-10T11:59:57.350Z
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
  
  import { describe, it, expect } from 'vitest';
  
  describe('Test Suite 1', () => {
      it('addition', () => {
      expect(1 + 1).to.equal(2);
      });
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/mocha/vitest/migrate-tests
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=RJbxDLL8OnSOS8b_dndDvw3loj4
f_cli-command: intuita mocha/vitest/migrate
f_framework: cms/framework/mocha.md
f_applicability-criteria: "`mocha` >= 9.0.0"
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: mocha-vitest-migrate
title: Mocha Vvitest - Migrate Tests from Mocha to Vitest
f_slug-name: mocha-vitest-migrate
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "5+ minutes/file"
tags: automations
updated-on: 2024-01-10T11:59:57.350Z
published-on: 2024-01-10T11:59:57.350Z
seo:
  title: Mocha Vvitest - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  og:title: Mocha Vvitest - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  twitter:title: Mocha Vvitest - Migrate Tests from Mocha to Vitest | Codemod.com Automations
  description: Run this codemod to upgrade your codebase from using mocha to vitest.
  twitter:card: Run this codemod to upgrade your codebase from using mocha to vitest.
---
Run this codemod to upgrade your codebase from using mocha to vitest.