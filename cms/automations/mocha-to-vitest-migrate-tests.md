---
created-on: 2023-12-18T14:39:14.938Z
f_long-description: |-
  ## Description

  Run this codemod to upgrade your codebase from using mocha to vitest.

  ## Example

  ### Before

  ```typescript
  import { expect } from 'chai';

  describe('Test Suite 1', () => {
      it('addition', () => {
      expect(1 + 1).to.equal(2);
      });
  });
  ```

  ### After

  ```typescript
  import { describe, it, expect } from 'vitest';

  describe('Test Suite 1', () => {
      it('addition', () => {
      expect(1 + 1).to.equal(2);
      });
  });
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/blob/main/codemods/mocha/vitest/migrate-tests
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=ixL8xbXt5GJlQmntTjYCF_7K7-Y
f_cli-command: codemod mocha/vitest/migrate-tests
f_framework: cms/framework/vitest.md
f_applicability-criteria: Mocha  >= 9.0.0
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: ember-app-controller-router-props
updated-on: 2023-12-18T14:39:14.959Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5+ minutes/file
date: 2023-12-18T14:39:14.981Z
f_slug-name: app-controller-router-props
title: Mocha to Vitest - Migrate Tests
published-on: 2023-12-18T14:39:14.970Z
f_labels:
  - cms/labels/mocha-to-vitest-migration.md
tags: automations
seo:
  title: Migrate Tests from Mocha to Vitest
  description: Run this codemod to upgrade your codebase from using mocha to vitest.
---
Run this codemod to upgrade your codebase from using mocha to vitest.