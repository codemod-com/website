---
created-on: 2024-01-10T11:59:57.910Z
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
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/app-directory-boilerplate
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=QKEdp-pofR9UnglrKAGDm1Oj6W0
f_cli-command: intuita next/13/app-directory-boilerplate
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-app-directory-boilerplate
title: Next V13 - App Directory Boilerplate
f_slug-name: next-13-app-directory-boilerplate
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-10T11:59:57.910Z
published-on: 2024-01-10T11:59:57.910Z
seo:
  title: Next V13 - App Directory Boilerplate | Codemod.com Automations
  og:title: Next V13 - App Directory Boilerplate | Codemod.com Automations
  twitter:title: Next V13 - App Directory Boilerplate | Codemod.com Automations
  description: The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.
  twitter:card: The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.
---
The first step to migrate your pages to the `app` directory is to provide a new file structure, respected by the App router.