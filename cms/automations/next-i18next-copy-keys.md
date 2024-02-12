---
created-on: 2023-12-22T13:34:26.118Z
published-on: 2023-12-22T13:34:26.118Z
f_long-description: >-
  ## Description


  This codemod copies specific keys from one translation namespace to another, for each of the supported languages. The codemod expects the following arguments:


  * `oldNamespace` is the name of the namespace from which the keys are taken,

  * `newNamespace` is the name of the namespace to which the keys are copied,

  * `keys` is a comma-separated list of keys.
    You need to pass these arguments using the [Codemod Arguments' settings](https://docs.codemod.com/docs/vs-code-extension/advanced-usage#set-codemod-arguments) in Codemod.com VS Code extension or [Codemod.com CLI](https://docs.codemod.com/docs/cli/quickstart).

  ### Before:


  #### .../en/common.json


  ```json

  {
  	"copyKey": "copyKeyEnglish",
  	"noopKey": "noopKeyEnglish"
  }

  ```


  #### .../en/new.json


  ```json

  {
  	"existingKey": "existingKeyEnglish"
  }

  ```


  ### After:


  #### .../en/common.json


  ```json

  {
  	"copyKey": "copyKeyEnglish",
  	"noopKey": "noopKeyEnglish"
  }

  ```


  #### .../en/new.json


  ```json

  {
  	"existingKey": "existingKeyEnglish",
  	"copyKey": "copyKeyEnglish"
  }

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next-i18next/copy-keys
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=SjMsX5HjVc-QOXnMZ3sE__LVV1Q
f_cli-command: intuita next-i18next/copy-keys
f_framework: cms/framework/next-js.md
f_codemod-engine: cms/codemod-engines/filemod.md
f_applicability-criteria: "`next-i18next > 14.x`"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: next-i18next-copy-keys
updated-on: 2023-12-22T13:34:26.118Z
f_change-mode-2: Autonomous
f_estimated-time-saving: ~1 minute/each key within each language file
date: 2023-12-22T13:36:11.061Z
f_slug-name: next-i18next-copy-keys
title: " i18Next - Copy Keys"
f_labels:
  - cms/labels/next-i18n.md
tags: automations
seo:
  title: Next.js - i18next Copy Keys
  og:title: Next.js - i18next Copy Keys
  twitter:title: Next.js - i18next Copy Keys
  description: This codemod copies specific keys from one translation namespace to
    another, for each of the supported languages.
  twitter:card: This codemod copies specific keys from one translation namespace
    to another, for each of the supported languages.
  og:image: /assets/images/next-i18n-copy-keys-automated-refactor.jpg
---
This codemod copies specific keys from one translation namespace to another, for each of the supported languages.