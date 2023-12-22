---
created-on: 2023-12-22T13:15:54.834Z
f_long-description: >-
  ## Description
  

  This codemod copies specific keys from one translation namespace to another, for each of the supported languages.
  The codemod expects the following arguments:
  -   `oldNamespace` is the name of the namespace from which the keys are taken,
  -   `newNamespace` is the name of the namespace to which the keys are copied,
  -   `keys` is a comma-separated list of keys.
  You need to pass these arguments using the [Codemod Arguments' settings](https://docs.intuita.io/docs/vs-code-extension/advanced-usage#set-codemod-arguments) in Intuita VS Code extension or [Intuita CLI](https://docs.intuita.io/docs/cli/quickstart).
  

  
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
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/next-i18next/copy-keys
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=SjMsX5HjVc-QOXnMZ3sE__LVV1Q
f_cli-command: intuita next-i18next/copy-keys
f_framework: cms/framework/next-i18next.md
f_applicability-criteria: "`next-i18next > 14.x`"
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-i18next-copy-keys
title: Next-i18next Vcopy-keys - next-i18next Copy Keys
f_slug-name: next-i18next-copy-keys
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minute/each key within each language file"
tags: automations
updated-on: 2023-12-22T13:15:54.834Z
published-on: 2023-12-22T13:15:54.834Z
seo:
  title: Next-i18next Vcopy-keys - next-i18next Copy Keys | Intuita Automations
  og:title: Next-i18next Vcopy-keys - next-i18next Copy Keys | Intuita Automations
  twitter:title: Next-i18next Vcopy-keys - next-i18next Copy Keys | Intuita Automations
  description: This codemod copies specific keys from one translation namespace to another, for each of the supported languages.
  twitter:card: This codemod copies specific keys from one translation namespace to another, for each of the supported languages.
---
This codemod copies specific keys from one translation namespace to another, for each of the supported languages.