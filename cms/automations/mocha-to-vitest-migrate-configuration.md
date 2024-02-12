---
created-on: 2023-12-18T14:34:24.351Z
f_long-description: >-
  ## Description


  Run this codemod to upgrade configuration files that need to be changed after migrating from `mocha` to `vitest`.


  ## Example


  ### `package.json`


  ### Before


  ```json

  {
    "name": "package-name",
    "dependencies": {
      "mocha": "^10.2.0",
      "some-mocha-plugin": "^10.0.4"
    },
    "devDependencies": {
      "mocha": "^10.2.0",
      "@types/mocha": "^10.0.4"
    },
    "main": "./dist/index.cjs",
    "types": "/dist/index.d.ts",
    "scripts": {
      "build:cjs": "cjs-builder ./src/index.ts",
      "test": "mocha"
    },
    "mocha": {
      "config-key": "config-value"
    },
    "files": [
      "README.md",
      "config.json",
      "./dist/index.cjs",
      "./index.d.ts"
    ],
    "type": "module"
  }

  ```


  ### After


  ```json

  {
    "name": "package-name",
    "dependencies": {},
    "devDependencies": {
      "vitest": "^1.0.1",
      "@vitest/coverage-v8": "^1.0.1"
    },
    "main": "./dist/index.cjs",
    "types": "/dist/index.d.ts",
    "scripts": {
      "build:cjs": "cjs-builder ./src/index.ts",
      "test": "vitest run",
      "coverage": "vitest run --coverage"
    },
    "files": [
      "README.md",
      "config.json",
      "./dist/index.cjs",
      "./index.d.ts"
    ],
    "type": "module"
  }

  ```


  ### `tsconfig.json`


  ### Before


  ```json

  {
    "compilerOptions": { "types": ["mocha"] },
    "include": [
      "./src/**/*.ts",
      "./src/**/*.js",
      "./test/**/*.ts",
      "./test/**/*.js"
    ]
  }

  ```


  ### After


  ```json

  {
    "compilerOptions": {},
    "include": [
      "./src/**/*.ts",
      "./src/**/*.js",
      "./test/**/*.ts",
      "./test/**/*.js"
    ]
  }

  ```


  ### `.mocharc`


  ### Before


  ```json

  {
    "loader": ["ts-node/esm"],
    "full-trace": true,
    "failZero": false,
    "bail": true,
    "spec": "./**/test.ts",
    "timeout": 5000
  }

  ```


  ### After


  `Removed`
f_github-link: https://github.com/codemod-com/codemod-registry/blob/main/codemods/mocha/vitest/migrate-configuration
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=-10xavJW4dcVcp6p_pjHxw9wfMA
f_cli-command: intuita mocha/vitest/migrate-configuration
f_framework: cms/framework/vitest.md
f_applicability-criteria: Mocha  >= 9.0.0
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: ember-app-controller-router-props
updated-on: 2023-12-18T14:34:24.373Z
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 5+ minutes/file
date: 2023-12-18T14:34:24.395Z
f_slug-name: app-controller-router-props
title: Mocha to Vitest - Migrate Configuration
published-on: 2023-12-18T14:34:24.384Z
f_labels:
  - cms/labels/mocha-to-vitest-migration.md
tags: automations
seo:
  title: Migrate Configuration from Mocha to Vitest | Codemod.com
  description: Run this automation to upgrade configuration files that need to be
    changed after migrating from `mocha` to `vitest`.
---
Run this codemod to upgrade configuration files that need to be changed after migrating from `mocha` to `vitest`.