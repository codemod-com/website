---
created-on: 2024-02-12T11:28:08.008Z
f_long-description: >-
  ## Description
  

  This codemod moves transforms imports from `next/server` to `next/og` for usage of [Dynamic OG Image Generation](https://nextjs.org/docs/app/building-your-application/optimizing/metadata#dynamic-image-generation).
  

  
  ### Before
  
  ```JavaScript
  
  import { ImageResponse } from 'next/server';
  
  ```
  
  ### After
  
  ```JavaScript
  
  import { ImageResponse } from 'next/og';
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/next/14/next-og-import
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=YH4iWtje8EfAlF0_ywnKrKTrQJY
f_cli-command: codemod next/14/next-og-import
f_framework: cms/framework/next-js.md
f_applicability-criteria: "Next.js version higher or equal to 14."
f_verified-codemod: false
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: next-14-next-og-import
title: Next V14 - Next OG Import
f_slug-name: next-14-next-og-import
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.008Z
published-on: 2024-02-12T11:28:08.008Z
seo:
  title: Next V14 - Next OG Import
  og:title: Next V14 - Next OG Import
  twitter:title: Next V14 - Next OG Import
  description: This codemod moves transforms imports from next/server` to `next/og` for usage of [Dynamic OG Image Generation](https://nextjs
  twitter:card: This codemod moves transforms imports from next/server` to `next/og` for usage of [Dynamic OG Image Generation](https://nextjs
---
This codemod moves transforms imports from `next/server` to `next/og` for usage of [Dynamic OG Image Generation](https://nextjs.org/docs/app/building-your-application/optimizing/metadata#dynamic-image-generation).