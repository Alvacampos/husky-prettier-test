# Basic project setup

This is a basic project setup example. with basic and standard rules.

## Installation

run `npm install`

## Basic setup

- Install husky (this will allow you to set up basic git hooks to prevent commits with convention errors):
  1. Run `npx husky-init && npm install`, go to `/.husky/pre-commit` and add `npx pretty-quick --staged` `npx prettier --check .`.
- Install prettier (this will enforce code format rules that husky will be able to use):

  1. Run `npm install --save-dev --save-exact prettier`.
  2. Run `echo {}> .prettierrc.json` to create a prettier config file

  ```
  {
    "trailingComma": "es5",
    "tabWidth": 4,
    "semi": false,
    "singleQuote": true
  }
  ```

  3. Add .prettierignore file with the following:

  ```
  # Post processed CSS
  app/styles
  # Caches
  .cache/

  # build outputs
  public
  build
  functions

  # binaries
  bin/
  ```

- Install eslint:
  1. Run `npm install --save-dev eslint-config-prettier`.
  2. Here you can run `npm install eslint -g` & `eslint --init` to use a default config like airbnb (one of the best).
  3. Add prettier to its rules
  ```
  {
  "extends": [
    "some-other-config-you-use",
    "prettier"
    ]
  }
  ```
