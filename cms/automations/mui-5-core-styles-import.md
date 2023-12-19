---
created-on: 2023-12-19T17:15:53.342Z
f_long-description: >-
  ## Description
  Renames private import from core/styles/* to core/styles..
  ### Before
  ```ts
  import { darken, lighten } from '@material-ui/core/styles/colorManipulator';
  import { Overrides } from '@material-ui/core/styles/overrides';
  import makeStyles from '@material-ui/core/styles/makeStyles';
  import { createTheme } from '@material-ui/core/styles';
  ```
  ### After
  ```ts
  import { createTheme, darken, lighten, Overrides, makeStyles } from '@material-ui/core/styles';
  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/mui/5/core-styles-import
f_vs-code-link: -
f_codemod-studio-link: -
f_cli-command: -
f_framework: cms/framework/mui.md
f_applicability-criteria: MUI version >= 4.0.0
f_verified-codemod: false
f_author: -
layout: "[automations].html"
slug: -
title: Core Styles Import
f_slug-name: -
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: ~5 minutes/occurrence
tags: automations
updated-on: 2023-12-19T17:15:53.342Z
published-on: 2023-12-19T17:15:53.342Z
seo: -
---
