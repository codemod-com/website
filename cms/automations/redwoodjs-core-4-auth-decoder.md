---
created-on: 2023-12-21T16:31:42.016Z
f_long-description: >-
  ## Description
  

  This codemod for RedwoodJS v4 automatically inserts an authDecoder property into the createGraphQLHandler call if it's not already present. It also adds an import statement for authDecoder from @redwoodjs/auth-auth0-api at the beginning of the file, ensuring that the necessary functionality for authentication is correctly integrated.
  

  ### Before
  
  ```ts
  import { createGraphQLHandler } from '@redwoodjs/graphql-server';
  
  import directives from 'src/directives/**/*.{js,ts}';
  import sdls from 'src/graphql/**/*.sdl.{js,ts}';
  import services from 'src/services/**/*.{js,ts}';
  
  import { logger } from 'src/lib/logger';
  import { db } from 'src/lib/db';
  
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
  import services from 'src/services/**/*.{js,ts}';
  
  import { logger } from 'src/lib/logger';
  import { db } from 'src/lib/db';
  
  export const handler = createGraphQLHandler({
    authDecoder: authDecoder,
    loggerConfig: { logger, options: {} },
    directives,
    sdls,
    services,
  
    onException: () => {
      // Disconnect from your database with an unhandled exception.
      db.$disconnect();
    }
  });
  ```
  
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/redwoodjs/core/4/auth-decoder
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=P-Ska-uPydbl8azQJ-cXmvwILbg
f_codemod-studio-link: n/a
f_cli-command: intuita redwoodjs/core/4/auth-decoder
f_framework: cms/framework/redwoodjs.md
f_applicability-criteria: RedwoodJS < v4.0.0
f_verified-codemod: false
f_author: cms/authors/redwoodjs.md
layout: "[automations].html"
slug: redwoodjs-core-4-auth-decoder
title: Redwoodjs Vcore - Auth Decoder
f_slug-name: redwoodjs-core-4-auth-decoder
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: ~5 minutes/occurrence
tags: automations
updated-on: 2023-12-21T16:31:42.016Z
published-on: 2023-12-21T16:31:42.016Z
seo: n/a
---