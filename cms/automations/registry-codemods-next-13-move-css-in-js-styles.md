---
created-on: 2024-01-31T16:23:09.047Z
f_long-description: >-
  ## Description
  

  This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.
  

  
  ### Before
  
  ```jsx
  
  const Head = () => {
  	return (
  		<head>
  			<style type="text/css">
  				{`
          body {
            margin: 0;
            padding: 0;
          }
        `}
  			</style>
  		</head>
  	);
  };
  
  export default Head;
  
  ```
  
  ### After
  The file gets transformed into:
  
  ```jsx
  
  import styles from 'Head.module.css';
  
  const Head = () => {
  	return <head className={styles['wrapper']}></head>;
  };
  
  export default Head;
  
  ```
  And the codemod creates the new file `Head.module.css` which contains:
  
  ```jsx
  
  body {
  	margin: 0;
  	padding: 0;
  }
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/next/13/move-css-in-js-styles
f_framework: cms/framework/registry.md
f_applicability-criteria: "Next.js version higher or equal to 13."
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Move CSS in JS Styles
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence."
tags: automations
updated-on: 2024-01-31T16:23:09.047Z
published-on: 2024-01-31T16:23:09.047Z
seo:
  title: Registry Vcodemods - Move CSS in JS Styles | Codemod.com Automations
  og:title: Registry Vcodemods - Move CSS in JS Styles | Codemod.com Automations
  twitter:title: Registry Vcodemods - Move CSS in JS Styles | Codemod.com Automations
  description: This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules
  twitter:card: This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules
---
This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.