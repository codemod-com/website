---
created-on: 2024-01-31T16:23:09.134Z
f_long-description: >-
  ## Description
  

  Since Next.js 13.4, you can use the following hooks from the `next/navigation` module:
    -   `useRouter`,
    -   `useSearchParams`,
    -   `usePathname`,
    -   `useParams`.
  These hooks replace the functionality available in the `useRouter` hook in the `next/hook` module, however, the behavior is distinct.
  This codemod allows you to migrate the `useRouter` hook to the new `useRouter` hook imported from `next/navigation`. This includes all usages of the `useRouter` hook which may be replaced with `useSearchParams` and `usePathname`.
  

  
  ### Before
  
  ```tsx
  
  import { useRouter } from 'next/router';
  
  function Component() {
  	const { query } = useRouter();
  	const { a, b, c } = query;
  }
  
  ```
  
  ### After
  
  ```tsx
  
  import { useParams, useSearchParams } from 'next/navigation';
  import { useCallback } from 'react';
  
  function Component() {
  	const params = useParams();
  	const searchParams = useSearchParams();
  	const getParam = useCallback(
  		(p: string) => params?.[p] ?? searchParams?.get(p),
  		[params, searchParams],
  	);
  
  	const a = getParam('a');
  	const b = getParam('b');
  	const c = getParam('c');
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/replace-next-router
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace Next Router
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:09.134Z
published-on: 2024-01-31T16:23:09.134Z
seo:
  title: Registry Vcodemods - Replace Next Router | Codemod.com Automations
  og:title: Registry Vcodemods - Replace Next Router | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace Next Router | Codemod.com Automations
  description: Since Next
  twitter:card: Since Next
---
Since Next.js 13.4, you can use the following hooks from the `next/navigation` module: