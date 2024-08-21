### <p align="center">React js frontend lint file</p>

In order to run this file, you'll need to add the following dev dependancies

```
npm install --save-dev npm install --save-dev eslint-plugin-unused-imports eslint-plugin-newline-destructuring eslint-plugin-imports-destructuring-newline @stylistic/eslint-plugin @stylistic/eslint-plugin-js eslint-plugin-react
```
Eslint file contents for react frontend

``` js
// .eslintrc.js

module.exports = {
  root: true,
  env: { browser: true, es2020: true },
  extends: [
    'eslint:recommended',
    'plugin:@typescript-eslint/recommended',
    'plugin:react-hooks/recommended'
  ],
  ignorePatterns: ['dist', '.eslintrc.cjs'],
  parser: '@typescript-eslint/parser',
  plugins: [
    'react-refresh',
    '@stylistic',
    '@stylistic/js',
    'unused-imports',
    'newline-destructuring',
    "imports-destructuring-newline",
    "react"
  ],
  rules: {
    'react-hooks/exhaustive-deps': "off",
    "@typescript-eslint/no-namespace": "off",
    'react-refresh/only-export-components': [
      'warn',
      { allowConstantExport: true },
    ],
    "unused-imports/no-unused-imports": "warn",
    "@typescript-eslint/no-explicit-any": "error",
    "@typescript-eslint/semi": "warn",
    "@stylistic/js/block-spacing": "warn",
    "@stylistic/js/arrow-spacing": "warn",
    "@stylistic/js/brace-style": "warn",
    "@stylistic/js/comma-spacing": [
      "warn",
      { "before": false, "after": true }],
    "@stylistic/js/indent": ["warn", {
            "SwitchCase": 1
    }],
    "@stylistic/js/padding-line-between-statements": [
      "warn",
      { "blankLine": "always", "prev": ["block", "block-like", "let", "const", "function"], "next": ["return", "block", "block-like"] },
      { "blankLine": "never", "prev": ["let", "const"], "next": ["let", "const"] },
      { "blankLine": "always", "prev": ["let", "const"], "next": ["function", "block", "block-like"] },
    ],
    "@stylistic/js/padded-blocks": ["error", "never"],
    "@stylistic/js/no-multiple-empty-lines": ["error", { "max": 1, "maxEOF": 1, "maxBOF": 0, }],
    "@stylistic/js/object-curly-newline": ["warn", {
      "ObjectExpression": { "multiline": true, "minProperties": 3, "consistent": true },
      "ObjectPattern": { "multiline": true, "minProperties": 3, "consistent": true },
      "ImportDeclaration": { "multiline": true, "minProperties": 5, "consistent": true },
      "ExportDeclaration": { "multiline": true, "minProperties": 5, "consistent": true }
    }],
    "@stylistic/js/object-property-newline": ["error", {
      "allowAllPropertiesOnSameLine": false
    }],
    "@stylistic/js/comma-dangle": ["error", "never"],
    "newline-destructuring/newline": ["error", {
      "items": 2
    }],
    "imports-destructuring-newline/import-declaration-newline": ["warn", {
      "minProperties": 5
    }],
    "imports-destructuring-newline/export-declaration-newline": ["warn"],
    "react/jsx-max-props-per-line": ["warn", {
      "maximum": { "single": 5, "multi": 1 },
    }],
    "react/jsx-first-prop-new-line": ["warn", "multiline-multiprop"]
  }
}
```
