---
created-on: 2023-12-22T11:32:17.758Z
f_long-description: >-
  ## Description
  

  Replace import for removed component in v5.
  

  
  ### Before
  
  ```TypeScript
  
  import { Avatar, BackTop, Comment, PageHeader } from 'antd';
  
  
  ```
  
  ### After
  
  ```TypeScript
  
  import { Comment } from '@ant-design/compatible';
  import { PageHeader } from '@ant-design/pro-layout';
  import { Avatar, FloatButton } from 'antd';
  
  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/antd/5/removed-component-migration
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=ZG4qJ0pLVV0_4Ei7sfVLt0uOZtQ
f_cli-command: intuita antd/5/removed-component-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: antd-5-removed-component-migration
title: Antd V5 - Removed Component Migration
f_slug-name: antd-5-removed-component-migration
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
tags: automations
updated-on: 2023-12-22T11:32:17.758Z
published-on: 2023-12-22T11:32:17.758Z
seo:
  title: Antd V5 - Removed Component Migration | Intuita Automations
  og:title: Antd V5 - Removed Component Migration | Intuita Automations
  twitter:title: Antd V5 - Removed Component Migration | Intuita Automations
  description: Replace import for removed component in v5.
  twitter:card: Replace import for removed component in v5.
---