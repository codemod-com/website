---
created-on: 2024-02-09T18:30:34.161Z
f_long-description: >-
  ## Description
  

  The following data fetching methods are no longer available in the `app` directory:
    -   `getStaticPaths`,
    -   `getServerSideProps`,
    -   `getStaticProps`.
  The codemod migrates the data fetching functions into the supported in the `app` directory:
    -   `getStaticPaths` -> `generateStaticParams`
    -   `getServerSideProps` -> `getData`
    -   `getStaticProps` -> `getData` (used in the component)
  If the `getStaticPaths` function has only one expression in the return statement, it will be inlined within the `nextData` function, otherwise it will remain unchanged.
  When migrating the `getServerSideProps` functions, the codemod assumes that only the `params` property of the first argument is used.
  It additionally adds types for aforementioned `params` and page props.
  It will also add the `revalidate` and `dynamicParams` route segment properties.
  

  
  ### Before
  
  ```jsx
  
  import PostLayout from '@/components/post-layout';
  
  export async function getStaticPaths() {
  	return {
  		paths: [{ params: { id: '1' } }, { params: { id: '2' } }],
  		fallback: 'blocking',
  	};
  }
  
  export async function getStaticProps({ params }) {
  	const res = await fetch(`https://.../posts/${params.id}`);
  	const post = await res.json();
  
  	return { props: { post } };
  }
  
  export default function Post({ post }) {
  	return <PostLayout post={post} />;
  }
  
  ```
  
  ### After
  
  ```jsx
  
  import { notFound, redirect } from 'next/navigation';
  import PostLayout from '@/components/post-layout';
  
  type Params = {
  	[key: string]: string | string[] | undefined,
  };
  
  type PageProps = {
  	params: Params,
  };
  
  export async function getStaticPaths() {
  	return {
  		paths: [{ params: { id: '1' } }, { params: { id: '2' } }],
  		fallback: 'blocking',
  	};
  }
  
  export async function generateStaticParams() {
  	return (await getStaticPaths({})).paths;
  }
  
  export async function getStaticProps({ params }) {
  	const res = await fetch(`https://.../posts/${params.id}`);
  	const post = await res.json();
  
  	return { props: { post } };
  }
  
  async function getData({ params }: { params: Params }) {
  	const result = await getStaticProps({ params });
  
  	if ('redirect' in result) {
  		redirect(result.redirect.destination);
  	}
  
  	if ('notFound' in result) {
  		notFound();
  	}
  
  	return 'props' in result ? result.props : {};
  }
  
  export default async function Post({ params }: PageProps) {
  	const { post } = await getData({ params });
  
  	return <PostLayout post={post} />;
  }
  
  export const dynamicParams = true;
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/next/13/remove-get-static-props
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=gqDiMZhaiz_RSzyfHeUueiYcGFI
f_cli-command: codemod next/13/remove-get-static-props
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version is greater or equal to 13.4."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: next-13-remove-get-static-props
title: Next V13 - Migrate Data Fetching Methods
f_slug-name: next-13-remove-get-static-props
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~2 minutes/occurrence"
tags: automations
updated-on: 2024-02-09T18:30:34.161Z
published-on: 2024-02-09T18:30:34.161Z
seo:
  title: Next V13 - Migrate Data Fetching Methods | Codemod.com Automations
  og:title: Next V13 - Migrate Data Fetching Methods | Codemod.com Automations
  twitter:title: Next V13 - Migrate Data Fetching Methods | Codemod.com Automations
  description: The following data fetching methods are no longer available in the app` directory
  twitter:card: The following data fetching methods are no longer available in the app` directory
---
The following data fetching methods are no longer available in the `app` directory: