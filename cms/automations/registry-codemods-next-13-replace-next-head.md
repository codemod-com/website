---
created-on: 2024-01-31T16:23:09.118Z
f_long-description: >-
  ## Description
  

  Generates a static metadata object based on meta tags managed by `next/head`.
  The codemod checks all the child components used in a page file and extracts all the meta tags defined within the `<Head>` component. Such tags are then moved to the very page file alongside the dependencies of the tags.
  

  
  ### Before:
  
  ```jsx
  
  // a page file
  import Meta from '../../components/a.tsx';
  	export default function Page() {
  		return <Meta />;
  }
  
  // component file
  import Head from 'next/head';
  import NestedComponent from '../components/b.tsx';
  export default function Meta() {
  	return (<>
  	<Head>
  		<title>title</title>
  	</Head>
  	<NestedComponent />
  	</>)
  }
  
  // nested component file
  import Head from 'next/head';
  
  export default function NestedComponent() {
  	return <Head>
  	<meta name="description" content="description" />
  	</Head>
  }
  
  export default NestedComponent;
  
  ```
  
  ### After:
  
  ```jsx
  
  // page file
  import { Metadata } from 'next';
  import Meta from '../../components/a.tsx';
  export const metadata: Metadata = {
  	title: `title`,
  	description: 'description',
  };
  export default function Page() {
  	return <Meta />;
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/replace-next-head
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version higher or equal to 13."
f_verified-codemod: false
f_author: cms/authors/vercel.md
layout: "[automations].html"
title: Registry Vcodemods - Replace Next Head
f_codemod-engine: cms/codemod-engines/filemod.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence"
tags: automations
updated-on: 2024-01-31T16:23:09.118Z
published-on: 2024-01-31T16:23:09.118Z
seo:
  title: Registry Vcodemods - Replace Next Head | Codemod.com Automations
  og:title: Registry Vcodemods - Replace Next Head | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace Next Head | Codemod.com Automations
  description: Generates a static metadata object based on meta tags managed by next/head
  twitter:card: Generates a static metadata object based on meta tags managed by next/head
---
Generates a static metadata object based on meta tags managed by `next/head`.