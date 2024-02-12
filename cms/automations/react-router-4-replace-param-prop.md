---
created-on: 2024-02-12T11:28:08.321Z
f_long-description: >-
  ## Description
  

  Replaces `params` prop passed by react-router with `match.params`.
  

  
  ### Before
  
  ```jsx
  
  const PostEdit = ({ params }) => (
  	<div>
  		<h1>Post {params.id}</h1>
  	</div>
  );
  
  ```
  
  ### After
  
  ```jsx
  
  const PostEdit = ({ match }) => (
  	<div>
  		<h1>Post {match.params.id}</h1>
  	</div>
  );
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/react-router/4/replace-param-prop
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=YI-kM-fKohkbQpdSYCuGOh3twE8
f_cli-command: codemod react-router/4/replace-param-prop
f_framework: cms/framework/react-router.md
f_applicability-criteria: "React Router version 3.x.y"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: react-router-4-replace-param-prop
title: React-router V4 - Replace params prop
f_slug-name: react-router-4-replace-param-prop
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~1 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.321Z
published-on: 2024-02-12T11:28:08.321Z
seo:
  title: React-router V4 - Replace params prop | Codemod.com Automations
  og:title: React-router V4 - Replace params prop | Codemod.com Automations
  twitter:title: React-router V4 - Replace params prop | Codemod.com Automations
  description: Replaces params` prop passed by react-router with `match
  twitter:card: Replaces params` prop passed by react-router with `match
---
Replaces `params` prop passed by react-router with `match.params`.