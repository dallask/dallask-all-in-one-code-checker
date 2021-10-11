# All in one code checker
---

## Overview

Provides set of libraries to easily setup code quality checks based ESlint, Stylelint, Prettier.


## Install

1. `npm install dallask-all-in-one-code-checker` The postinstall script will copy default configs and create check scripts.

1. If you do not see needed scripts in your package.json file, just copy them from file: ./node_modules/dallask-all-in-one-code-checker/package.json

```
"scripts": {
     "stylelint:total": "stylelint '**/*.scss'",
     "stylelint:current": "stylelint $(git diff --name-status | grep '\\.scss$' | grep -v \"^[RD]\" | awk '{ print $2 }')",
     "stylelint:total:fix": "stylelint '**/*.scss' --fix",
     "stylelint:current:fix": "stylelint --fix $(git diff --name-status | grep '\\.scss$' | grep -v \"^[RD]\" | awk '{ print $2 }')",
     "prettier:total": "prettier '**/*' --check",
     "prettier:current": "prettier --check $(git diff --name-status | grep '\\.scss$\\|\\.js$' | grep -v \"^[RD]\" | awk '{ print $2 }')",
     "prettier:total:fix": "prettier '**/*' --write",
     "prettier:current:fix": "prettier --write $(git diff --name-status | grep '\\.scss$\\|\\.js$' | grep -v \"^[RD]\" | awk '{ print $2 }')",
     "eslint:total": "eslint '**/*.js'",
     "eslint:current": "eslint $(git diff --name-status | grep '\\.js$' | grep -v \"^[RD]\" | awk '{ print $2 }')",
     "eslint:total:fix": "eslint '**/*.js' --fix",
     "eslint:current:fix": "eslint --fix $(git diff --name-status | grep '\\.js$' | grep -v \"^[RD]\" | awk '{ print $2 }')"
   }
```

## Features

1. [ESLint](https://eslint.org) 
1. [Stylelint](https://stylelint.io)  
1. [Prettier](https://prettier.io) 

## NPM Scripts

You can use next scripts to check and fix your files:

    Stylelint:
    stylelint:total - stylelint check for all project files
    stylelint:total:fix - stylelint fix for all project files
    stylelint:current - stylelint check for project files that were changed
    stylelint:current:fix - stylelint fix for project files that were changed
    
    Prettier:
    prettier:total - prettier check for all project files
    prettier:total:fix - prettier fix for all project files
    prettier:current - prettier check for project files that were changed
    prettier:current:fix - prettier fix for project files that were changed
    
    ESLint:
    eslint:total - eslint check for all project files
    eslint:total:fix - eslint fix for all project files
    eslint:current - eslint check for project files that were changed
    eslint:current:fix - prettier fix for project files that were changed
   
    Just run `npm run script_name` in root directory.

