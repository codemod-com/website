---
created-on: 2023-12-18T14:39:14.938Z
published-on: 2023-12-18T14:39:14.970Z
f_long-description: |-
  ## Description

  Run this codemod to upgrade your codebase from using mocha to vitest.

  ## Example

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
f_github-link: https://github.com/intuita-inc/codemod-registry/blob/main/codemods/mocha/vitest/migrate-tests
f_cli-command: intuita mocha/vitest/migrate-tests
f_framework: cms/framework/vitest.md
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_applicability-criteria: Mocha  >= 9.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: ember-app-controller-router-props
updated-on: 2023-12-18T14:39:14.959Z
f_change-mode-2: Assistive
f_estimated-time-saving: 5+ minutes/file
date: 2023-12-18T14:39:14.981Z
f_slug-name: app-controller-router-props
title: Mocha to Vitest - Migrate Tests
f_labels:
  - cms/labels/mocha-to-vitest-migration.md
tags: automations
seo:
  title: Migrate Tests from Mocha to Vitest| Intuita Automations
  og:title: Migrate Tests from Mocha to Vitest| Intuita Automations
  twitter:title: Migrate Tests from Mocha to Vitest| Intuita Automations
  description: Run this codemod to upgrade your codebase from using mocha to vitest.
  twitter:card: Run this codemod to upgrade your codebase from using mocha to vitest.
  og:image: /assets/images/mocha-to-vitest-migrate-tests.jpg
---
Run this codemod to upgrade your codebase from using mocha to vitest.