---
created-on: 2023-12-22T11:32:17.776Z
f_long-description: >-
  ## Description


  Replace message.warn with message.warning. Replace notification.close with notification.destroy.


  ### Before


  ```TypeScript

  import { message, notification } from 'antd';

  const App = () => {
    const [messageApi, contextHolder] = message.useMessage();
    const onClick1 = () => {
     message.warn();

    }
    const onClick2 = () => {
     messageApi.warn();
    };

    const [notificationApi] = notification.useNotification();
    const onClick3 = () => {
     notification.close();
    }
    const onClick4 = () => {
     notificationApi.close();
    };

    return <>{contextHolder}</>;
  };

  ```


  ### After


  ```TypeScript

  import { message, notification } from 'antd';

  const App = () => {
    const [messageApi, contextHolder] = message.useMessage();
    const onClick1 = () => {
     message.warning();
    }
    const onClick2 = () => {
     messageApi.warning();
    };

    const [notificationApi] = notification.useNotification();
    const onClick3 = () => {
     notification.destroy();
    }
    const onClick4 = () => {
     notificationApi.destroy();
    };

    return <>{contextHolder}</>;
  };

  ```
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/antd/5/removed-static-method-migration
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=kGFeVKZNWhdp1Al8BJ03ZYs_T-s
f_cli-command: intuita antd/5/removed-static-method-migration
f_framework: cms/framework/antd.md
f_applicability-criteria: Ant Design >= 5.0.0
f_verified-codemod: false
f_author: cms/authors/ant-design.md
layout: "[automations].html"
slug: antd-5-removed-static-method-migration
updated-on: 2023-12-22T13:15:54.805Z
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: Up to 1 minutes/occurrence
date: 2023-12-22T11:56:17.490Z
f_slug-name: antd-5-removed-static-method-migration
title: Ant Design V5 - Removed Static Method Migration
published-on: 2023-12-22T11:32:17.777Z
f_labels:
  - cms/labels/ant-design-v5-upgrade.md
tags: automations
seo:
  title: Antd V5 - Removed Static Method Migration | Codemod.com
  og:title: Antd V5 - Removed Static Method Migration | Codemod.com
  twitter:title: Antd V5 - Removed Static Method Migration | Codemod.com
  description: Replace message.warn with message.warning.
  twitter:card: Replace message.warn with message.warning.
---
Replace message.warn with message.warning. Replace notification.close with notification.destroy.