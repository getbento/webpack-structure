# Webpack Structure

This document outlines the structure for Webpack based React applications.

## Feature Complete Single Page Applications

```
├── .babelrc
├── .eslintrc
├── .gitignore
├── README.md
├── dist
│   └── manifest.json
├── package.json
├── src
│   ├── base
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   ├── containers
│   │   ├── layouts
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   ├── renderRoutes.js
│   │   │   └── routes.js
│   │   └── ui_components
│   │       ├── Global.js
│   │       └── Theme.js
│   ├── index.html
│   └── index.js
├── webpack.config.babel.js
└── yarn.lock
```

## Multifeature Single Page Applciations

```
├── .babelrc
├── .eslintrc
├── .gitignore
├── README.md
├── dist
│   └── manifest.json
├── package.json
├── src
│   ├── base
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   ├── containers
│   │   ├── layouts
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   ├── renderRoutes.js
│   │   │   └── routes.js
│   │   └── ui_components
│   │       ├── Global.js
│   │       └── Theme.js
│   ├── <app_name>
│   │   ├── actions
│   │   │   └── index.js
│   │   ├── components
│   │   ├── containers
│   │   ├── layouts
│   │   ├── reducers
│   │   │   ├── errors.js
│   │   │   ├── index.js
│   │   ├── routes
│   │   │   ├── renderRoutes.js
│   │   │   └── routes.js
│   │   └── ui_components
│   │       ├── Global.js
│   │       └── Theme.js
│   ├── index.html
│   └── index.js
├── webpack.config.babel.js
└── yarn.lock
```
