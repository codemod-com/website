---
created-on: 2023-12-22T11:32:17.741Z
f_long-description: >-
  ## Description


  Comment out the style file import from antd (in js file).


  ### Before


  ```TypeScript

  import 'antd/es/auto-complete/style'; import 'antd/lib/button/style/index.less'; import 'antd/dist/antd.compact.min.css';

  ```


  ### After


  ```TypeScript

  // import 'antd/es/auto-complete/style'; // import 'antd/lib/button/style/index.less'; // import 'antd/dist/antd.compact.min.css';

  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/antd/5/remove-style-import
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=ovpw9tnJRJOsXRJSawZ4ycQhWGQ
f_cli-command: intuita antd/5/remove-style-import
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: antd-5-remove-style-import
updated-on: 2023-12-22T11:32:17.741Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
date: 2023-12-22T11:43:41.703Z
f_slug-name: antd-5-remove-style-import
title: Ant Design V5 - Remove Style Import
published-on: 2023-12-22T11:32:17.741Z
f_labels:
  - cms/labels/ant-design-v5-upgrade.md
tags: automations
seo:
  title: Antd V5 - Remove Style Import | Intuita Automations
  og:title: Antd V5 - Remove Style Import | Intuita Automations
  twitter:title: Antd V5 - Remove Style Import | Intuita Automations
  description: Comment out the style file import from antd (in js file).
  twitter:card: Comment out the style file import from antd (in js file).
---
Comment out the style file import from antd (in js file).