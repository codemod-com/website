---
created-on: 2023-12-18T14:29:04.416Z
f_long-description: >-
  ## Description


  This recipe is a set of codemods that will upgrade your project from using `mocha` to `vitest`.


  The recipe includes the following codemods:


  * [migrate-configuration](https://github.com/intuita-inc/codemod-registry/tree/main/codemods/mocha/vitest/migrate-configuration)

  * [migrate-tests](https://github.com/intuita-inc/codemod-registry/tree/main/codemods/mocha/vitest/migrate-tests)


  NOTE: if you are not using vitest default `.spec.*` or `.test.*` file names, then you won't be able to run your tests upon migrating. To mitigate this and add your own set of globs, create `vite.config.ts` file in the root of your project and add the following configuration, replacing `**/test/*.ts` with your own globs:


  ```typescript

  import { configDefaults, defineConfig } from 'vitest/config';


  export default defineConfig({
  	test: {
  		include: [...configDefaults.include, '**/test/*.ts'],
  	},
  });

  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/blob/main/codemods/mocha/vitest/recipe
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=oDAjaOrkUfLtuw4nNXnfIHLEL-o
f_cli-command: intuita mocha/vitest/recipe
f_framework: cms/framework/vitest.md
f_applicability-criteria: Mocha  >= 9.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: ember-app-controller-router-props
updated-on: 2023-12-18T14:29:04.433Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: 5+ minutes/file
date: 2023-12-18T14:29:04.470Z
f_slug-name: app-controller-router-props
title: Mocha to Vitest - Migration Recipe
published-on: 2023-12-18T14:29:04.446Z
f_labels:
  - cms/labels/mocha-to-vitest-migration.md
tags: automations
seo:
  title: Mocha to Vitest Migration Recipe | Intuita Automations
  og:title: Mocha to Vitest Migration Recipe | Intuita Automations
  twitter:title: Mocha to Vitest Migration Recipe | Intuita Automations
  description: This recipe is a set of codemods that will upgrade your project
    from using mocha to vitest.
  twitter:card: This recipe is a set of codemods that will upgrade your project
    from using mocha to vitest.
  og:image: /assets/images/mocha-to-vitest-migration-recipe.jpg
---
This recipe is a set of codemods that will upgrade your project from using `mocha` to `vitest`.