---
created-on: 2023-12-22T11:32:17.722Z
f_long-description: >-
  ## Description
  

  This codemod changes the way the component props are applied.
  

  
  ### Before
  
  ```TypeScript
  
  import { Tag } from 'antd';
  
  const Component = () => {
    const [visible, setVisible] = useState(false);
  
    return <Tag visible={visible} />;
  };
  
  ```
  
  ### After
  
  ```TypeScript
  
  import { Tag } from 'antd';
  
  const Component = () => {
    const [visible, setVisible] = useState(false);
  
    return (visible ? <Tag /> : null);
  };
  
  ```
f_github-link: https://github.com/intuita-inc/codemod-registry/tree/main/codemods/antd/5/props-changed-migration
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=z9CCNbzBKfYVGQ_FZJNG6nrmRTs
f_cli-command: intuita antd/5/props-changed-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: true
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: antd-5-props-changed-migration
title: Antd V5 - Props Changed Migration
f_slug-name: antd-5-props-changed-migration
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
tags: automations
updated-on: 2023-12-22T11:32:17.723Z
published-on: 2023-12-22T11:32:17.723Z
seo:
  title: Antd V5 - Props Changed Migration | Intuita Automations
  og:title: Antd V5 - Props Changed Migration | Intuita Automations
  twitter:title: Antd V5 - Props Changed Migration | Intuita Automations
  description: This codemod changes the way the component props are applied.
  twitter:card: This codemod changes the way the component props are applied.
---