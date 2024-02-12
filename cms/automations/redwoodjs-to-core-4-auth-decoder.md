---
created-on: 2024-02-12T11:28:07.863Z
f_long-description: >-
  ## Description
  

  This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call if it's not already present. It also adds an import statement for `authDecoder` from `@redwoodjs/auth-auth0-api` at the beginning of the file, ensuring that the necessary functionality for authentication is correctly integrated.
  

  
  ### Before
  
  ```ts
  
  import { createGraphQLHandler } from '@redwoodjs/graphql-server';
  import directives from 'src/directives/**/*.{js,ts}';
  import sdls from 'src/graphql/**/*.sdl.{js,ts}';
  import { db } from 'src/lib/db';
  import { logger } from 'src/lib/logger';
  import services from 'src/services/**/*.{js,ts}';
  
  export const handler = createGraphQLHandler({
  	loggerConfig: { logger, options: {} },
  	directives,
  	sdls,
  	services,
  	onException: () => {
  		// Disconnect from your database with an unhandled exception.
  		db.$disconnect();
  	},
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { authDecoder } from '@redwoodjs/auth-auth0-api';
  import { createGraphQLHandler } from '@redwoodjs/graphql-server';
  import directives from 'src/directives/**/*.{js,ts}';
  import sdls from 'src/graphql/**/*.sdl.{js,ts}';
  import { db } from 'src/lib/db';
  import { logger } from 'src/lib/logger';
  import services from 'src/services/**/*.{js,ts}';
  
  export const handler = createGraphQLHandler({
  	authDecoder: authDecoder,
  	loggerConfig: { logger, options: {} },
  	directives,
  	sdls,
  	services,
  
  	onException: () => {
  		// Disconnect from your database with an unhandled exception.
  		db.$disconnect();
  	},
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/redwoodjs/core/4/auth-decoder
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=P-Ska-uPydbl8azQJ-cXmvwILbg
f_cli-command: codemod redwoodjs/core/4/auth-decoder
f_framework: cms/framework/redwoodjs.md
f_applicability-criteria: "RedwoodJS < v4.0.0"
f_verified-codemod: false
f_author: cms/authors/rajasegar-chandran.md
layout: "[automations].html"
slug: redwoodjs-core-4-auth-decoder
title: Redwoodjs to core - Auth Decoder
f_slug-name: redwoodjs-core-4-auth-decoder
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~6 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:07.863Z
published-on: 2024-02-12T11:28:07.863Z
seo:
  title: Redwoodjs to core - Auth Decoder | Codemod.com Automations
  og:title: Redwoodjs to core - Auth Decoder | Codemod.com Automations
  twitter:title: Redwoodjs to core - Auth Decoder | Codemod.com Automations
  description: This codemod for RedwoodJS v4 automatically inserts an authDecoder` property into the `createGraphQLHandler` call if it's not already present
  twitter:card: This codemod for RedwoodJS v4 automatically inserts an authDecoder` property into the `createGraphQLHandler` call if it's not already present
---
This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call if it's not already present. It also adds an import statement for `authDecoder` from `@redwoodjs/auth-auth0-api` at the beginning of the file, ensuring that the necessary functionality for authentication is correctly integrated.