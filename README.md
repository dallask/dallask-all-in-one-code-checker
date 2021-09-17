# All in one code checker
---

## Overview

Provides set of libraries to easily setup code quality checks based ESlint, Stylelint, Prettier.


## Install

1. `npm install dallask-all-in-one-code-checker` The postinstall script will copy default configs and create check scripts.

1. If you do not see needed scripts in the your package.json file, just copy them from file: ./node_modules/dallask-all-in-one-code-checker/package.json

```
"scripts": {
     "stylelint": "stylelint '**/*.scss'",
     "stylelint:fix": "stylelint '**/*.scss' --fix",
     "prettier": "prettier '**/*' --check",
     "prettier:fix": "prettier '**/*' --write",
     "eslint": "eslint '**/*.js'",
     "eslint:fix": "eslint '**/*.js' --fix"
   }
```

## Features

1. [ESLint](https://eslint.org) 
1. [Stylelint](https://stylelint.io)  
1. [Prettier](https://prettier.io) 

## NPM Scripts

You can use next scripts to check and fix your files:

    stylelint           
    stylelint:fix
    prettier
    prettier:fix
    eslint
    eslint:fix 
   
    Just run `npm run script_name` in root directory.

