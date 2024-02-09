---
created-on: 2024-02-09T18:30:34.631Z
f_long-description: >-
  ## Description
  

  This codemod removes unused i18n translations.
  

  
  ### Before:
  
  ```jsx
  
  import { useLocale } from '@calcom/lib/hooks/useLocale';
  
  export default function A() {
  	const { t } = useLocale();
  
  	return <p>{t('key1')}</p>;
  }
  
  ```
  
  ### After:
  
  ```jsx
  
  {
  	"key1": "key1",
  	"key2": "key2"
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/i18n
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=BAny38trthdC9B2S1HoJw7YCKMo
f_cli-command: codemod i18n/remove-unused-translations
f_framework: cms/framework/i18n.md
f_applicability-criteria: "Any version of i18n."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: i18n-remove-unused-translations
title: I18n to README.md - Replace API Routes
f_slug-name: i18n-remove-unused-translations
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.631Z
published-on: 2024-02-09T18:30:34.631Z
seo:
  title: I18n to README.md - Replace API Routes | Codemod.com Automations
  og:title: I18n to README.md - Replace API Routes | Codemod.com Automations
  twitter:title: I18n to README.md - Replace API Routes | Codemod.com Automations
  description: This codemod removes unused i18n translations
  twitter:card: This codemod removes unused i18n translations
---
This codemod removes unused i18n translations.