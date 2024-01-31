---
created-on: 2024-01-31T16:23:08.284Z
f_long-description: >-
  ## Description
  

  The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.
  This is attempted by this codemod, which reads the contents of your `pages` directory and creates the placeholder files.
  The placeholder files define the basic layout and page structure.
  The boilerplate includes the following:
    -   placeholder `page.tsx` and `layout.tsx` files which define a UI unique to a route.
  If the codemod detects that a `getStaticProps` function is not used, it will be removed. Otherwise, it will remove the `export` keyword from the function definition.
  

  If you have the following directory:
  
  ```null
  
    pages
    ├── a.tsx
    └── b
          └── c.tsx
  
  
  ```
  The codemod will generate the following corresponding directory:
  
  ```null
  
    app
    ├── a
          └── page.tsx
          └── layout.tsx
    └── b
          └── c
                └── page.tsx
                └── layout.tsx
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/cal.com/app-directory-boilerplate-calcom
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - App Directory Boilerplate for Cal.com
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.284Z
published-on: 2024-01-31T16:23:08.284Z
seo:
  title: Registry Vcodemods - App Directory Boilerplate for Cal.com | Codemod.com Automations
  og:title: Registry Vcodemods - App Directory Boilerplate for Cal.com | Codemod.com Automations
  twitter:title: Registry Vcodemods - App Directory Boilerplate for Cal.com | Codemod.com Automations
  description: The first step to migrate your pages to the app` directory is to provide a new file structure, respected by the App router
  twitter:card: The first step to migrate your pages to the app` directory is to provide a new file structure, respected by the App router
---
The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.