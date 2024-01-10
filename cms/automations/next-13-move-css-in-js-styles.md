---
created-on: 2024-01-10T11:59:57.967Z
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
f_github-link: https://github.com/codemod-com/codemod-registry/tree/main/codemods/next/13/move-css-in-js-styles
f_vs-code-link: vscode://intuita.intuita-vscode-extension/showCodemod?chd=fPpa1xqB9D0AN4VazhrRkrWri9g
f_cli-command: intuita next/13/move-css-in-js-styles
f_framework: cms/framework/next.md
f_applicability-criteria: "Next.js version higher or equal to 13."
f_verified-codemod: false
f_author: cms/authors/intuita.md
layout: "[automations].html"
slug: next-13-move-css-in-js-styles
title: Next V13 - Move CSS in JS Styles
f_slug-name: next-13-move-css-in-js-styles
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Assistive
f_estimated-time-saving: "~5 minutes/occurrence."
tags: automations
updated-on: 2024-01-10T11:59:57.967Z
published-on: 2024-01-10T11:59:57.967Z
seo:
  title: Next V13 - Move CSS in JS Styles | Codemod.com Automations
  og:title: Next V13 - Move CSS in JS Styles | Codemod.com Automations
  twitter:title: Next V13 - Move CSS in JS Styles | Codemod.com Automations
  description: This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.
  twitter:card: This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.
---
This highly experimental codemod moves the CSS-in-JS styles into the CSS Modules.