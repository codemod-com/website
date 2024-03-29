---
title: MSW V2 - MSW Upgrade Recipe
created-on: 2023-11-16T14:11:04.212Z
updated-on: 2023-11-17T15:17:39.056Z
published-on: 2023-11-17T15:18:58.613Z
f_long-description: >-
  ## Description


  This recipe is a set of codemods that will upgrade your project from using msw v1 to v2.

  The recipe includes the following codemods:


  * [imports](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/imports)

  * [type-args](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/type-args)

  * [request-changes](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/request-changes)

  * [ctx-fetch](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/ctx-fetch)

  * [req-passthrough](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/req-passthrough)

  * [response-usages](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/response-usages)

  * [callback-signature](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/callback-signature)

  * [lifecycle-events-signature](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/lifecycle-events-signature)

  * [print-handler](https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/print-handler)


  ### FNs


  This recipe does not change the signatures of MSW handlers, if they were called using a custom factory function, for example to provide more type-safety or else. For example, the following code will only be partially updated:


  ```typescript

  export function mockFactory<T extends MyComplexType>(
    url: string,
    resolver: MyResolverType,
  ) {
    return rest.get(url, resolver);
  }

  const handlers = [
    mockFactory('/some/url', (req, res, ctx) => {
      return res(
        ctx.status(200),
      );
    }),
  ];

  ```


  ### Links for more info


  * [MSW v1 to v2 Migration Guide](https://mswjs.io/docs/migrations/1.x-to-2.x/)
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/msw/2/upgrade-recipe
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=GZo687pOCc0ICc9ptHSWPJTErcM
f_cli-command: codemod msw/2/upgrade-recipe
f_framework: cms/framework/msw.md
f_codemod-engine: cms/codemod-engines/ts-morph.md
f_change-mode-2: Assistive
f_estimated-time-saving: Depending on the size of the project, this recipe can
  save up to 6 hours of dedicated work and more.
f_applicability-criteria: MSW version >= 1.0.0
f_labels:
  - cms/labels/msw-v1-v2.md
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: msw-upgrade-recipe
tags: automations
date: 2023-11-20T14:53:04.294Z
f_slug-name: msw-upgrade-recipe
seo:
  title: MSW V2 Upgrade Recipe
  description: This recipe is a set of automations that will upgrade your project
    from using msw v1 to v2.
---
This recipe is a set of automations that will upgrade your project from using msw v1 to v2.