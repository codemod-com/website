---
created-on: 2023-12-19T18:50:06.276Z
f_long-description: >-
  ## Description
  

  Renames private import from core/styles/* to core/styles
  

  ### Before
  
  ```typescript
  import { darken, lighten } from '@material-ui/core/styles/colorManipulator';
  import { Overrides } from '@material-ui/core/styles/overrides';
  import makeStyles from '@material-ui/core/styles/makeStyles';
  import { createTheme } from '@material-ui/core/styles';
  ```
  
  ### After
  
  ```typescript
  import { createTheme, darken, lighten, Overrides, makeStyles } from '@material-ui/core/styles';
  ```
  
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/mui/5/core-styles-import
f_vs-code-link: vscode://intuita.intuita-vscode-extension/cases/u4y5Xb9WZe33RAdnBDvsHaNvQMk
f_codemod-studio-link: n/a
f_cli-command: intuita mui/5/core-styles-import
f_framework: cms/framework/mui.md
f_applicability-criteria: MUI version >= 4.0.0
f_verified-codemod: false
f_author: cms/authors/mui.md
layout: "[automations].html"
slug: mui-5-core-styles-import
title: Core Styles Import
f_slug-name: mui-5-core-styles-import
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: ~5 minutes/occurrence
tags: automations
updated-on: 2023-12-19T18:50:06.276Z
published-on: 2023-12-19T18:50:06.276Z
seo: n/a
---
