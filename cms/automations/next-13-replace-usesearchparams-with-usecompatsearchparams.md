---
created-on: 2023-11-30T17:13:54.590Z
f_long-description: >-
  ## Description


  A recent update in Next.js brought a breaking change: the useSearchParams hook no longer includes params. To ease the migration, the new useCompatSearchParams hook can be used. This hook mimics the behavior of the old useSearchParams in two ways:


  * it includes both params and searchParams

  * params overwrite any conflicting values in searchParams


  ## Example


  ### Before


  ```typescript

  import { useSearchParams } from 'next/navigation';


  export async function Component() {
  	const params = useSearchParams();
  	return <div>My Component</div>;
  }

  ```


  ### After


  ```typescript

  import { useCompatSearchParams } from 'hooks/utils';


  export async function Component() {
  	const params = useCompatSearchParams();

  	return <div>My Component</div>;
  }

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/blob/main/codemods/next/13/replace-use-search-params
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=mdYqG7HyVLFNaAp4S60Ws19TQSQ
f_cli-command: intuita next/13/replace-use-search-params
f_framework: cms/framework/next-js.md
f_applicability-criteria: Next.js version is greater or equal to 13.4.
f_verified-codemod: false
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: app-router-recipe
title: Next.js Replace useSearchParams with useCompatSearchParams
updated-on: 2023-11-30T17:13:54.602Z
published-on: 2023-11-30T17:13:54.611Z
f_slug-name: replace-use-search-params
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: 2 minutes/occurrence
f_labels:
  - cms/labels/next-js-app-router-migration.md
tags: automations
date: 2023-11-30T17:13:54.620Z
seo:
  title: Next.js Replace useSearchParams
  description: This automation replaces `useSearchParams` with `useCompatSearchParams`.
---
This automation replaces `useSearchParams` with `useCompatSearchParams`.