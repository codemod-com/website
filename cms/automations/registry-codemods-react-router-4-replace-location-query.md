---
created-on: 2024-02-01T18:03:45.294Z
f_long-description: >-
  ## Description
  

  This codemod replaces instances of `location.query` with `parse(location.search)`, where `parse` is a function imported from `query-string`.
  

  
  ### Before
  
  ```jsx
  
  const List = ({ location }) => (
  	<div>
  		<h1>{location.query.sort}</h1>
  	</div>
  );
  
  ```
  
  ### After
  
  ```jsx
  
  import { parse } from 'query-string';
  
  const List = ({ location }) => (
  	<div>
  		<h1>{parse(location.search).sort}</h1>
  	</div>
  );
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/apps/registry/codemods/react-router/4/replace-location-query
f_framework: cms/framework/registry.md
f_applicability-criteria: "React Router version 3.x.y"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
title: Registry Vcodemods - Replace Location Query
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-02-01T18:03:45.294Z
published-on: 2024-02-01T18:03:45.294Z
seo:
  title: Registry Vcodemods - Replace Location Query | Codemod.com Automations
  og:title: Registry Vcodemods - Replace Location Query | Codemod.com Automations
  twitter:title: Registry Vcodemods - Replace Location Query | Codemod.com Automations
  description: This codemod replaces instances of location
  twitter:card: This codemod replaces instances of location
---
This codemod replaces instances of `location.query` with `parse(location.search)`, where `parse` is a function imported from `query-string`.