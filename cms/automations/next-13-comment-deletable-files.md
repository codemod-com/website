---
created-on: 2024-01-10T11:59:57.947Z
f_long-description: >-
  ## Description
  

  This codemod is recommended when migrating from the `/pages` to the `/app` directory.
  It adds a comment to files that should be deleted and migrated to different files during the migration process.
  Namely, such are the following files:
    -   `_document.*`,
    -   `_app.*`,
    -   `_error.*`.
  

  
  ### Before
  
  ```jsx
  
  import 'highlight.js/styles/default.css';
  import 'swagger-ui-react/swagger-ui.css';
  
  import '../styles/globals.css';
  
  function MyApp({ Component, pageProps }) {
  	return <Component {...pageProps} />;
  }
  
  export default MyApp;
  
  ```
  
  ### After
  
  ```jsx
  
  /*This file should be deleted. Please migrate its contents to appropriate files*/
  import 'highlight.js/styles/default.css';
  import 'swagger-ui-react/swagger-ui.css';
  
  import '../styles/globals.css';
  
  function MyApp({ Component, pageProps }) {
  	return <Component {...pageProps} />;
  }
  
  export default MyApp;
  
  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/comment-deletable-files
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=BaHE4pik14OhABrBRaAUohzhcs0
f_cli-command: intuita next/13/comment-deletable-files
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version higher or equal to 13.4"
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-comment-deletable-files
title: Next V13 - Comment Deletable Files
f_slug-name: next-13-comment-deletable-files
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "The purpose of this codemod is to guide the user into the files that should be migrated away, which should equal ~5 minutes total of estimated time saving."
tags: automations
updated-on: 2024-01-10T11:59:57.947Z
published-on: 2024-01-10T11:59:57.947Z
seo:
  title: Next V13 - Comment Deletable Files | Codemod.com Automations
  og:title: Next V13 - Comment Deletable Files | Codemod.com Automations
  twitter:title: Next V13 - Comment Deletable Files | Codemod.com Automations
  description: This codemod is recommended when migrating from the `/pages` to the `/app` directory.
  twitter:card: This codemod is recommended when migrating from the `/pages` to the `/app` directory.
---
This codemod is recommended when migrating from the `/pages` to the `/app` directory.