---
created-on: 2024-01-31T16:23:08.991Z
f_long-description: >-
  ## Description
  

  The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.
  This is attempted by this codemod, which reads the contents of your `pages` directory and creates the placeholder files.
  The placeholder files define the basic layout and page structure.
  The boilerplate includes the following:
    -   placeholder `page.tsx` and `layout.tsx` files which define a UI unique to a route.
    -   the placeholder `app/layout.tsx` file which replaces `pages/_app.tsx` and `pages/_document.tsx` files.
    -   the placeholder `error.tsx` file which replaces `pages/_error.tsx` files.
    -   the placeholder `not-found.tsx` file which replaces `pages/404.tsx` files.
  If the codemod detects that a `getStaticProps` function is not used, it will be removed. Otherwise, it will remove the `export` keyword from the function definition.
  

  If you have the following directory:
  
  ```null
  
    pages
    ├── _app.tsx
    ├── _document.tsx
    ├── _error.tsx
    ├── 404.tsx
    ├── a.tsx
    └── b
          └── c.tsx
  
  
  ```
  The codemod will generate the following corresponding directory:
  
  ```null
  
    app
    ├── page.tsx
    ├── layout.tsx
    ├── error.tsx
    ├── not-found.tsx
    ├── a
          └── page.tsx
    └── b
          └── c
                └── page.tsx
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/app-directory-boilerplate
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - App Directory Boilerplate
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.991Z
published-on: 2024-01-31T16:23:08.991Z
seo:
  title: Registry Vcodemods - App Directory Boilerplate | Codemod.com Automations
  og:title: Registry Vcodemods - App Directory Boilerplate | Codemod.com Automations
  twitter:title: Registry Vcodemods - App Directory Boilerplate | Codemod.com Automations
  description: The first step to migrate your pages to the app` directory is to provide a new file structure, respected by the App router
  twitter:card: The first step to migrate your pages to the app` directory is to provide a new file structure, respected by the App router
---
The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.