---
created-on: 2024-02-12T11:28:07.992Z
f_long-description: >-
  ## Description
  

  This codemod migrates certain viewport metadata to `viewport` export.
  

  
  ### Before
  
  ```jsx
  
  export const metadata = {
  	title: 'My App',
  	themeColor: 'dark',
  	viewport: {
  		width: 1,
  	},
  };
  
  ```
  
  ### After
  
  ```jsx
  
  export const metadata = {
  	title: 'My App',
  };
  
  export const viewport = {
  	width: 1,
  	themeColor: 'dark',
  };
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/next/14/metadata-to-viewport-export
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=hCw9Zucqpf__QgZRCVDUvzSMdeE
f_cli-command: codemod next/14/metadata-to-viewport-export
f_framework: cms/framework/next-js.md
f_applicability-criteria: "Next.js version higher or equal to 14."
f_verified-codemod: false
f_author: cms/authors/vercel.md
layout: "[automations].html"
slug: next-14-metadata-to-viewport-export
title: Next V14 - Metadata to Viewport Export
f_slug-name: next-14-metadata-to-viewport-export
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:07.992Z
published-on: 2024-02-12T11:28:07.992Z
seo:
  title: Next V14 - Metadata to Viewport Export | Codemod.com Automations
  og:title: Next V14 - Metadata to Viewport Export | Codemod.com Automations
  twitter:title: Next V14 - Metadata to Viewport Export | Codemod.com Automations
  description: This codemod migrates certain viewport metadata to viewport` export
  twitter:card: This codemod migrates certain viewport metadata to viewport` export
---
This codemod migrates certain viewport metadata to `viewport` export.