---
created-on: 2024-01-31T16:23:08.446Z
f_long-description: >-
  ## Description
  

  Following the original msw upgrade guide, the signature of the request handler have changed. This codemod hard replaces the callback signature to the new one and cleans up unused variables.
  NOTE: This codemod should be applied after running all the other codemods present in the `upgrade-recipe` that are related to `req`, `res`, `ctx` objects. On its own, this codemod makes no sense to be run, and will most likely not do what you want.
  
  
  ### WARNING
  
  This codemod runs `.fixUnusedIdentifiers()` on a source file you are running it on. This would remove any unused declarations in the file. This is due to atomicity of this mod, which blindly inserts the callback structure into each msw handler callback and then cleans up the variables that are not used.
  

  
  ### Before
  
  ```ts
  
  import { http } from 'msw';
  
  http.get('/resource', (req, res, ctx) => {
  	return HttpResponse.json({ id: 'abc-123' });
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { http } from 'msw';
  
  http.get('/resource', () => {
  	return HttpResponse.json({ id: 'abc-123' });
  });
  
  ```
  
  ### Before
  
  ```ts
  
  import { http } from 'msw';
  
  http.get('/resource', (req, res, ctx) => {
  	const userCookie = cookies.user;
  	const url = new URL(request.url);
  
  	doSomething(url);
  	userCookie.doSomething();
  
  	return HttpResponse.json({ id: 'abc-123' });
  });
  
  ```
  
  ### After
  
  ```ts
  
  import { http } from 'msw';
  
  http.get('/resource', ({ request, cookies }) => {
  	const userCookie = cookies.user;
  	const url = new URL(request.url);
  
  	doSomething(url);
  	userCookie.doSomething();
  
  	return HttpResponse.json({ id: 'abc-123' });
  });
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/msw/2/callback-signature
f_framework: cms/framework/registry.md
f_applicability-criteria: "MSW version >= 1.0.0"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace MSW handler signature
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "Up to 10 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.446Z
published-on: 2024-01-31T16:23:08.446Z
seo:
  title: Registry Vcodemods - Replace MSW handler signature | Codemod.com Automations
  og:title: Registry Vcodemods - Replace MSW handler signature | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace MSW handler signature | Codemod.com Automations
  description: Following the original msw upgrade guide, the signature of the request handler have changed
  twitter:card: Following the original msw upgrade guide, the signature of the request handler have changed
---
Following the original msw upgrade guide, the signature of the request handler have changed. This codemod hard replaces the callback signature to the new one and cleans up unused variables.