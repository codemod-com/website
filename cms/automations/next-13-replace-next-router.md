---
created-on: 2024-01-10T11:59:58.004Z
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
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/replace-next-router
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=-wqkAQr7ILgYeTRozWTEgiUvmSY
f_cli-command: intuita next/13/replace-next-router
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-replace-next-router
title: Next V13 - Replace Next Router
f_slug-name: next-13-replace-next-router
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:58.004Z
published-on: 2024-01-10T11:59:58.004Z
seo:
  title: Next V13 - Replace Next Router | Codemod.com Automations
  og:title: Next V13 - Replace Next Router | Codemod.com Automations
  twitter:title: Next V13 - Replace Next Router | Codemod.com Automations
  description: Since Next.js 13.4, you can use the following hooks from the `next/navigation` module:
  twitter:card: Since Next.js 13.4, you can use the following hooks from the `next/navigation` module:
---
Since Next.js 13.4, you can use the following hooks from the `next/navigation` module: