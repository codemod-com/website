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

  import { Comment } from '@ant-design/compatible'; import { PageHeader } from '@ant-design/pro-layout'; import { Avatar, FloatButton } from 'antd';

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/antd/5/removed-component-migration
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=ZG4qJ0pLVV0_4Ei7sfVLt0uOZtQ
f_cli-command: intuita antd/5/removed-component-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: false
f_author: cms/authors/ant-design.md
layout: "[automations].html"
slug: antd-5-removed-component-migration
updated-on: 2023-12-22T13:15:54.773Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
date: 2023-12-22T11:48:15.198Z
f_slug-name: antd-5-removed-component-migration
title: Ant Design V5 - Removed Component Migration
published-on: 2023-12-22T11:32:17.758Z
f_labels:
  - cms/labels/ant-design-v5-upgrade.md
tags: automations
seo:
  title: Antd V5 - Removed Component Migration | Codemod.com
  og:title: Antd V5 - Removed Component Migration | Codemod.com
  twitter:title: Antd V5 - Removed Component Migration | Codemod.com
  description: Replace import for removed component in v5.
  twitter:card: Replace import for removed component in v5.
---
Replace import for removed component in v5.