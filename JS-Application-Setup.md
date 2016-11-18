# Creating a new JavaScript Application

## What do you need?
  * Package manager: NPM (Bower, Yarn)
  * Task Runner: Webpack (Grunt, Gulp)
  * Test Runner: Karma
  * Framework: React (Angular, Angular2)
  * Test Framework: Jasmine

## Config the new app
  * `mkdir newapp && cd newapp`
  * `git init`
  * `npm init`
  * `npm install -g webpack`
  * `npm install --save-dev webpack`
  * `npm install --save react react-dom`
  * `npm install --save-dev karma karma-jasmine karma-phantomjs-launcher karma-phantomjs-shim karma-webpack`
  * `npm install --save -dev phantomjs-prebuilt`
  * `npm install --save-dev babel-loader babel-core babel-polyfill babel-preset-es2015`
  * `npm install --save-dev node-sass sass-loader css-loader style-loader html-loader`
  * `npm install --save-dev browser-sync browser-sync-spa`
  
 ...
 This can all be defined in a single package.json file.
 And Yarn is better for installing dependencies.
