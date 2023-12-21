---
created-on: 2023-12-21T16:50:53.999Z
f_long-description: >-
  # Auth Decoder


  ## Description


  This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call if it's not already present. It also adds an import statement for `authDecoder` from `@redwoodjs/auth-auth0-api` at the beginning of the file, ensuring that the necessary functionality for authentication is correctly integrated.


  ## Example


  ### Before


  ```typescript

  import { createGraphQLHandler } from '@redwoodjs/graphql-server';


  import directives from 'src/directives/**/*.{js,ts}';

  import sdls from 'src/graphql/**/*.sdl.{js,ts}';

  import services from 'src/services/**/*.{js,ts}';


  import { db } from 'src/lib/db';

  import { logger } from 'src/lib/logger';


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


  ```typescript

  import { authDecoder } from '@redwoodjs/auth-auth0-api';

  import { createGraphQLHandler } from '@redwoodjs/graphql-server';


  import directives from 'src/directives/**/*.{js,ts}';

  import sdls from 'src/graphql/**/*.sdl.{js,ts}';

  import services from 'src/services/**/*.{js,ts}';


  import { db } from 'src/lib/db';

  import { logger } from 'src/lib/logger';


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
f_cli-command: intuita redwoodjs/core/4/auth-decoder
f_framework: cms/framework/redwoodjs.md
f_applicability-criteria: RedwoodJS < v4.0.0
f_verified-codemod: false
f_author: cms/authors/redwoodjs.md
layout: "[automations].html"
slug: redwoodjs-core-4-auth-decoder
updated-on: 2023-12-21T16:50:53.999Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: ~6 minutes/occurrence
date: 2023-12-21T16:57:01.202Z
f_slug-name: redwoodjs-core-4-auth-decoder
title: Redwoodjs V4 - Auth Decoder
published-on: 2023-12-21T16:50:53.999Z
tags: automations
seo:
  title: Redwoodjs V4 - Auth Decoder | Intuita Automations
  og:title: Redwoodjs V4 - Auth Decoder | Intuita Automations
  twitter:title: Redwoodjs V4 - Auth Decoder | Intuita Automations
  description: This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call.
  twitter:card: This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call.
---
This codemod for RedwoodJS v4 automatically inserts an `authDecoder` property into the `createGraphQLHandler` call.
