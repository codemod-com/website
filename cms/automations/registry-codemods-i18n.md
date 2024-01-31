---
created-on: 2024-01-31T16:23:08.334Z
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
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/i18n
f_framework: cms/framework/registry.md
f_applicability-criteria: "Any version of i18n."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace API Routes
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:08.334Z
published-on: 2024-01-31T16:23:08.334Z
seo:
  title: Registry Vcodemods - Replace API Routes | Codemod.com Automations
  og:title: Registry Vcodemods - Replace API Routes | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace API Routes | Codemod.com Automations
  description: This codemod removes unused i18n translations
  twitter:card: This codemod removes unused i18n translations
---
This codemod removes unused i18n translations.