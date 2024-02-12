---
created-on: 2024-02-12T11:28:08.308Z
f_long-description: >-
  ## Description
  

  This codemod replaces instances of `location.query` with `parse(location.search)`, where `parse` is a function imported from `query-string`.
  

  
  ### Before
  
  ```JavaScript
  
  const List = ({ location }) => (
  	<div>
  		<h1>{location.query.sort}</h1>
  	</div>
  );
  
  ```
  
  ### After
  
  ```JavaScript
  
  import { parse } from 'query-string';
  
  const List = ({ location }) => (
  	<div>
  		<h1>{parse(location.search).sort}</h1>
  	</div>
  );
  
  ```
f_github-link: https://github.com/codemod-com/codemod/tree/main/apps/registry/codemods/react-router/4/replace-location-query
f_vs-code-link: vscode://codemod.codemod-vscode-extension/showCodemod?chd=eyHOwZNJqdSRNKdi25EkGzfK374
f_cli-command: codemod react-router/4/replace-location-query
f_framework: cms/framework/react-router.md
f_applicability-criteria: "React Router version 3.x.y"
f_verified-codemod: true
f_author: cms/authors/codemod-com.md
layout: "[automations].html"
slug: react-router-4-replace-location-query
title: React-router V4 - Replace Location Query
f_slug-name: react-router-4-replace-location-query
f_codemod-engine: cms/codemod-engines/jscodeshift.md
f_change-mode-2: Autonomous
f_estimated-time-saving: "~3 minutes/occurrence"
tags: automations
updated-on: 2024-02-12T11:28:08.308Z
published-on: 2024-02-12T11:28:08.308Z
seo:
  title: React-router V4 - Replace Location Query
  description: This codemod replaces instances of location
---
This codemod replaces instances of `location.query` with `parse(location.search)`, where `parse` is a function imported from `query-string`.