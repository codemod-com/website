---
created-on: 2024-01-31T16:23:09.182Z
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
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/upsert-use-client-directive
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Upsert Use Client Directive
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:09.182Z
published-on: 2024-01-31T16:23:09.182Z
seo:
  title: Registry Vcodemods - Upsert Use Client Directive | Codemod.com Automations
  og:title: Registry Vcodemods - Upsert Use Client Directive | Codemod.com Automations
  twitter:title: Registry Vcodemods - Upsert Use Client Directive | Codemod.com Automations
  description: Since Next
  twitter:card: Since Next
---
Since Next.js 13.4, you can mark the files that contain only client-side code with the `use client` directive at the top.