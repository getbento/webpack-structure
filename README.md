# Webpack Structure

This document outlines the structure for Webpack based React applications.

## Feature Complete Single Page Applications

This structure is intended for all new, self contained React applications.

```bash
project_name
├── .babelrc
├── .eslintignore
├── .eslintrc
├── .gitignore
├── README.md
├── dist
│   └── manifest.json
├── package.json
├── src
│   ├── app
│   │   ├── __tests__
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   │   └── <ExampleComponent>.js
│   │   ├── constants
│   │   │   └── actionTypes.js
│   │   ├── containers
│   │   │   └──  <ExampleContainer>.js
│   │   ├── layouts
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   ├── renderRoutes.js
│   │   │   └── routes.js
│   │   ├── store
│   │   │   └── configureStore.js
│   │   └── ui_components
│   │       ├── Global.js
│   │       └── Theme.js
│   ├── index.html
│   └── index.js
├── webpack.config.js
└── yarn.lock
```

## Multifeature Single Page Applciations

This structure is intended for large, multi feature applications.

```bash
project_name
├── .babelrc
├── .eslintignore
├── .eslintrc
├── .gitignore
├── README.md
├── config
│   ├── webpack.base.config.js
│   ├── webpack.local.config.js
│   ├── webpack.production.config.js
│   ├── webpack.test.config.js
│   └── manifest.json
├── dist
│   └── manifest.json
├── package.json
├── src
│   ├── base
│   │   ├── __tests__
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   │   └── <ExampleComponent>.js
│   │   ├── constants
│   │   │   └── actionTypes.js
│   │   ├── containers
│   │   │   └──  <ExampleContainer>.js
│   │   ├── layouts
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   ├── renderRoutes.js
│   │   │   └── routes.js
│   │   ├── store
│   │   │   └── configureStore.js
│   │   └── ui_components
│   │       ├── Global.js
│   │       └── Theme.js
│   ├── <app_name>
│   │   ├── __tests__
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   │   └── <ExampleComponent>.js
│   │   ├── constants
│   │   │   └── actionTypes.js
│   │   ├── containers
│   │   │   └──  <ExampleContainer>.js
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   └── routes.js
│   │   └── ui_components
│   │       └── <Example>.js
│   ├── index.html
│   ├── index.js
│   └── static
│       ├── fonts
│       ├── images
│       └── scss (legacy scss while all ui components are created)
├── webpack.config.js
└── yarn.lock
```

In this structure there are a few key points:

*   The `base` application holds a number of constants and imports functions/constants from subapplciations. For example, the `base/routes.js` file imports all other routes from subapplications such that the `index.js` or `webpack.config.babel.js` only imports one in route creation.
*   For applications that use more than one Babel configuration (vanilla, ES6+, etc) combined, it is important to rename the `webpack.config.js` to `webpack.config.babel.js`
*   There should be a set of common styled-components inside of the `base` application. Each app that requires one off `styled-components` should be placed inside the subapplicatoins `ui_components` directory.
