---
created-on: 2024-01-31T16:23:08.377Z
f_long-description: >-
  ## Description
  

  Run this codemod to upgrade configuration files that need to be changed after migrating from `mocha` to `vitest`.
  

  
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
  	"files": ["README.md", "config.json", "./dist/index.cjs", "./index.d.ts"],
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
  	"files": ["README.md", "config.json", "./dist/index.cjs", "./index.d.ts"],
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
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/mocha/vitest/migrate-configuration
f_framework: cms/framework/registry.md
f_applicability-criteria: "`mocha` >= 9.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Migrate Configuration from Mocha to Vitest
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "5+ minutes/file"
tags: automations
updated-on: 2024-01-31T16:23:08.377Z
published-on: 2024-01-31T16:23:08.377Z
seo:
  title: Registry Vcodemods - Migrate Configuration from Mocha to Vitest | Codemod.com Automations
  og:title: Registry Vcodemods - Migrate Configuration from Mocha to Vitest | Codemod.com Automations
  twitter:title: Registry Vcodemods - Migrate Configuration from Mocha to Vitest | Codemod.com Automations
  description: Run this codemod to upgrade configuration files that need to be changed after migrating from mocha` to `vitest
  twitter:card: Run this codemod to upgrade configuration files that need to be changed after migrating from mocha` to `vitest
---
Run this codemod to upgrade configuration files that need to be changed after migrating from `mocha` to `vitest`.