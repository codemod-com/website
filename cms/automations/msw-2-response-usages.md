---
created-on: 2024-01-10T11:59:57.527Z
f_long-description: >-
  ## Description
  

  To send a response from MSW handler, one would previously use something like `res(ctx.text("Hello world"))`. In msw v2, this is achieved by returning a native WebAPI Response object. msw v2 conveniently exposes a `HttpResponse` function that has useful methods for creating just that object with a desired body. This codemod replaces the old `res` calls with the new `HttpResponse` function calls and a bunch of ctx utilities that usually go with it. See examples below.
  This codemod does not remove unused properties on the callback signature due to the fact that there are more changes in other codemods included in the `upgrade-recipe` that rely on it. To apply these changes, you will have to run the recipe or run a `callback-signature` codemod that will do only that and replace all the references of old signature arguments.
  

  
  ### Before
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.json({ id: "abc-123" }),
      ctx.cookie("roses", "red"),
      ctx.cookie("violets", "blue"),
      ctx.set("X-Custom", "value")
    );
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.json({ id: 'abc-123' }, {
      headers: {
        'X-Custom': 'value',
        'Set-Cookie': 'roses=red;violets=blue;',
      },
    });
  });
  
  ```
  
  ### Before
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.text("Hello world!"),
      ctx.delay(500),
      ctx.status(401)
    );
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { rest, delay } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    await delay(500);
  
    return HttpResponse.text("Hello world", {
      status: 401,
    });
  });
  
  ```
  
  ### Before
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return res(
      ctx.body('Hello world!'),
      ctx.set('Content-Type', 'text/plain'),
    );
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { rest, delay } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.text("Hello world");
  });
  
  ```
  
  ### Before
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return res(ctx.text('Hello world!'));
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { rest } from 'msw';
  
  rest.get('/user', (req, res, ctx) => {
    return HttpResponse.text("Hello world");
  });
  
  ```
  
  ### Before
  
  ```ts
  
  graphql.query('GetUser', (req, res, ctx) => {
    return res(
      ctx.data({
        user: { firstName: 'John' },
      }),
      ctx.errors([
        { message: `Failed to login:  user "${username}" does not exist` },
      ]),
      ctx.extensions({
        requestId: 'abc-123',
      })
    )
  })
  
  ```
  
  ### After
  
  ```ts
  
  graphql.query('GetUser', (req, res, ctx) => {
    return HttpResponse.json(
      data: {
        user: { firstName: 'John' },
      },
      errors: [
        { message: `Failed to login:  user "${username}" does not exist` },
      ],
      extensions: {
        requestId: 'abc-123',
      },
    )
  })
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/response-usages
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=xAFwkrXvZOF0QbeiBWcvwm8WpDI
f_cli-command: intuita msw/2/response-usages
f_framework: cms/framework/msw.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-response-usages
title: Msw V2 - Update Response Usages
f_slug-name: msw-2-response-usages
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "Up to 10 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.527Z
published-on: 2024-01-10T11:59:57.527Z
seo:
  title: Msw V2 - Update Response Usages | Codemod.com Automations
  og:title: Msw V2 - Update Response Usages | Codemod.com Automations
  twitter:title: Msw V2 - Update Response Usages | Codemod.com Automations
  description: To send a response from MSW handler, one would previously use something like `res(ctx.text("Hello world"))`. In msw v2, this is achieved by returning a native WebAPI Response object. msw v2 conveniently exposes a `HttpResponse` function that has useful methods for creating just that object with a desired body. This codemod replaces the old `res` calls with the new `HttpResponse` function calls and a bunch of ctx utilities that usually go with it. See examples below.
  twitter:card: To send a response from MSW handler, one would previously use something like `res(ctx.text("Hello world"))`. In msw v2, this is achieved by returning a native WebAPI Response object. msw v2 conveniently exposes a `HttpResponse` function that has useful methods for creating just that object with a desired body. This codemod replaces the old `res` calls with the new `HttpResponse` function calls and a bunch of ctx utilities that usually go with it. See examples below.
---
To send a response from MSW handler, one would previously use something like `res(ctx.text("Hello world"))`. In msw v2, this is achieved by returning a native WebAPI Response object. msw v2 conveniently exposes a `HttpResponse` function that has useful methods for creating just that object with a desired body. This codemod replaces the old `res` calls with the new `HttpResponse` function calls and a bunch of ctx utilities that usually go with it. See examples below.