---
created-on: 2023-12-21T17:56:46.986Z
f_long-description: >-
  ## Description
  

  There is a change to generic type interface of `rest.method()` calls. This codemod puts the generic arguments in the correct order to keep type safety.
  
  
  ### WARNING
  
  This codemod runs `.fixUnusedIdentifiers()` on a target source file. This would remove any unused declarations in the file. This is due to the atomicity of this codemod, which blindly inserts the callback structure into each msw handler callback and then cleans up the variables that are not used anymore.
  

  
  ### Before
  
  ```ts
  
  http.get<ReqBodyType, PathParamsType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });
  
  ```
  
  ### After
  
  ```ts
  
  http.get<PathParamsType, ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });
  
  ```
  
  ### Before
  
  ```ts
  
  http.get<ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });
  
  ```
  
  ### After
  
  ```ts
  
  http.get<any, ReqBodyType>('/resource', (req, res, ctx) => {
    return res(ctx.json({ firstName: 'John' }));
  });
  
  ```
  
  ### Before
  
  ```ts
  
  const handlers: RestHandler<DefaultBodyType>[] = [
    http.get('/resource', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ];
  
  ```
  
  ### After
  
  ```ts
  
  const handlers: HttpHandler[] = [
    http.get<any, DefaultBodyType>('/resource', (req, res, ctx) => {
      return res(ctx.json({ firstName: 'John' }));
    }),
  ];
  
  ```
  
  ### Before
  
  ```ts
  
  export function mockFactory(
    url: string,
    resolver: ResponseResolver<
      MockedRequest<{ id: string }>,
      RestContext,
      Awaited<ImportedPromiseBodyType>
    >,
  ) {
    return http.get(url, resolver);
  };
  
  ```
  
  ### After
  
  ```ts
  
  export function mockFactory(
    url: string,
    resolver: ResponseResolver<
      HttpRequestResolverExtras<PathParams>,
      { id: string },
      Awaited<ImportedPromiseBodyType>
    >,
  ) {
    return http.get(url, resolver);
  };
  
  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/msw/2/type-args
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=6rdxdJ7YioUlKoq-z-4iFPeN3Rs
f_cli-command: intuita msw/2/type-args
f_framework: cms/framework/msw.md
f_applicability-criteria: MSW version >= 1.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: msw-2-type-args
title: Msw V2 - Move Generic Arguments and Body Type Casts
f_slug-name: msw-2-type-args
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: ~15 minutes/occurrence
tags: automations
updated-on: 2023-12-21T17:56:46.986Z
published-on: 2023-12-21T17:56:46.986Z
seo:
  title: Msw V2 - Move Generic Arguments and Body Type Casts | Intuita Automations
  og:title: Msw V2 - Move Generic Arguments and Body Type Casts | Intuita Automations
  twitter:title: Msw V2 - Move Generic Arguments and Body Type Casts | Intuita Automations
  description: There is a change to generic type interface of `rest.method()` calls. This codemod puts the generic arguments in the correct order to keep type safety.
  twitter:card: There is a change to generic type interface of `rest.method()` calls. This codemod puts the generic arguments in the correct order to keep type safety.
---