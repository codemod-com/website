---
created-on: 2024-02-12T11:28:07.934Z
f_long-description: >-
  ## Description
  

  Renames private import from `core/styles/*` to `core/styles`
  

  
  ### Before
  
  ```typescript
  
  import { createTheme } from '@material-ui/core/styles';
  import { darken, lighten } from '@material-ui/core/styles/colorManipulator';
  import makeStyles from '@material-ui/core/styles/makeStyles';
  import { Overrides } from '@material-ui/core/styles/overrides';
  
  ```
  
  ### After
  
  ```typescript
  
  import {
  	createTheme,
  	darken,
  	lighten,
  	makeStyles,
  	Overrides,
  } from '@material-ui/core/styles';
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/mui/5/core-styles-import
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=u4y5Xb9WZe33RAdnBDvsHaNvQMk
f_cli-command: codemod mui/5/core-styles-import
f_framework: cms/framework/mui.md
f_applicability-criteria: "MUI version >= 4.0.0"
f_verified-codemod: false
f_author: cms/authors/mui.md
layout: "[automations].html"
slug: mui-5-core-styles-import
title: Mui V5 - Core Styles Import
f_slug-name: mui-5-core-styles-import
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:07.934Z
published-on: 2024-02-12T11:28:07.934Z
seo:
  title: Mui V5 - Core Styles Import
  description: Renames private import from core/styles/*` to `core/styles
---
Renames private import from `core/styles/*` to `core/styles`