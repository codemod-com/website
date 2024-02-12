---
created-on: 2023-12-22T11:32:17.722Z
f_long-description: |-
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
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/antd/5/props-changed-migration
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=z9CCNbzBKfYVGQ_FZJNG6nrmRTs
f_cli-command: intuita antd/5/props-changed-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: false
f_author: cms/authors/ant-design.md
layout: "[automations].html"
slug: antd-5-props-changed-migration
updated-on: 2023-12-22T13:15:54.718Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
date: 2023-12-22T11:48:14.131Z
f_slug-name: antd-5-props-changed-migration
title: Ant Design V5 - Props Changed Migration
published-on: 2023-12-22T11:32:17.723Z
f_labels:
  - cms/labels/ant-design-v5-upgrade.md
tags: automations
seo:
  title: Antd V5 - Props Changed Migration
  description: This codemod changes the way the component props are applied.
---
This codemod changes the way the component props are applied.