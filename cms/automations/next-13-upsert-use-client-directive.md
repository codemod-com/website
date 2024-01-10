---
created-on: 2024-01-10T11:59:58.024Z
f_long-description: >-
  ## Description
  

  Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.
  The codemod will look for identifiers and string literals common for files that contain client-side code, such as React hooks or event handlers. On the other hand, it will not upsert any directive should it spot elements indicating server-side code.
  The codemod will not remove the existing `use client` directive even if it would suggest otherwise due to the code in question.
  

  
  ### Before
  
  ```jsx
  
  import { useState } from 'react';
  
  export default function Page() {
  	const [x, setX] = useState('');
  
  	return x;
  }
  
  ```
  
  ### After
  
  ```jsx
  
  'use client';
  import { useState } from 'react';
  
  export default function Page() {
  	const [x, setX] = useState('');
  
  	return x;
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/upsert-use-client-directive
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=f_fR6Z-Q5qlxnPnHK5-tpeNckVw
f_cli-command: intuita next/13/upsert-use-client-directive
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-upsert-use-client-directive
title: Next V13 - Upsert Use Client Directive
f_slug-name: next-13-upsert-use-client-directive
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:58.024Z
published-on: 2024-01-10T11:59:58.024Z
seo:
  title: Next V13 - Upsert Use Client Directive | Codemod.com Automations
  og:title: Next V13 - Upsert Use Client Directive | Codemod.com Automations
  twitter:title: Next V13 - Upsert Use Client Directive | Codemod.com Automations
  description: Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.
  twitter:card: Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.
---
Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.