---
created-on: 2024-02-12T11:28:07.978Z
f_long-description: >-
  ## Description
  

  This codemod copies specific keys from one translation namespace to another, for each of the supported languages.
  The codemod expects the following arguments:
    -   `oldNamespace` is the name of the namespace from which the keys are taken,
    -   `newNamespace` is the name of the namespace to which the keys are copied,
    -   `keys` is a comma-separated list of keys.
  You need to pass these arguments using the [Codemod Arguments' settings](https://docs.codemod.com/docs/vs-code-extension/advanced-usage#set-codemod-arguments) in Codemod VSCode extension or [Codemod CLI](https://docs.codemod.com/docs/cli/quickstart).
  

  
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
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/next-i18next/copy-keys
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=SjMsX5HjVc-QOXnMZ3sE__LVV1Q
f_cli-command: codemod next-i18next/copy-keys
f_framework: cms/framework/next-i18next.md
f_applicability-criteria: "`next-i18next > 14.x`"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: next-i18next-copy-keys
title: Next-i18next to copy-keys - Next-i18next Copy Keys
f_slug-name: next-i18next-copy-keys
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~1 minute/each key within each language file"
tags: automations
updated-on: 2024-02-12T11:28:07.978Z
published-on: 2024-02-12T11:28:07.978Z
seo:
  title: Next-i18next to copy-keys - Next-i18next Copy Keys | Codemod.com Automations
  og:title: Next-i18next to copy-keys - Next-i18next Copy Keys | Codemod.com Automations
  twitter:title: Next-i18next to copy-keys - Next-i18next Copy Keys | Codemod.com Automations
  description: This codemod copies specific keys from one translation namespace to another, for each of the supported languages
  twitter:card: This codemod copies specific keys from one translation namespace to another, for each of the supported languages
---
This codemod copies specific keys from one translation namespace to another, for each of the supported languages.