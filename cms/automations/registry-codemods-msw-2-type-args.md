---
created-on: 2024-01-31T16:23:08.628Z
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
  }
  
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
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/type-args
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Move Generic Arguments and Body Type Casts
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~15 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.628Z
published-on: 2024-01-31T16:23:08.628Z
seo:
  title: Registry Vcodemods - Move Generic Arguments and Body Type Casts | Codemod.com Automations
  og:title: Registry Vcodemods - Move Generic Arguments and Body Type Casts | Codemod.com Automations
  twitter:title: Registry Vcodemods - Move Generic Arguments and Body Type Casts | Codemod.com Automations
  description: There is a change to generic type interface of rest
  twitter:card: There is a change to generic type interface of rest
---
There is a change to generic type interface of `rest.method()` calls. This codemod puts the generic arguments in the correct order to keep type safety.