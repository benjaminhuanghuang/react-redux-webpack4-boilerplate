## Webpack dependencies
```
    npm i -D webpack webpack-cli webpack-dev-server 
    npm i -D @babel/core @babel/preset-env @babel/preset-react @babel/preset-stage-2 babel-loader
```

- webpack: We need Webpack to bundle our code.

- webpack-cli: We will be using some CLI features for Webpack to make our life easier while writing some scripts.

- webpack-dev-server: Creating server. This is only meant to be used in the development environment, and not for production. 

- @babel/preset-env: This package behaves exactly the same as @babel/preset-latest (or @babel/preset-es2015, 

- @babel/preset-es2016, and @babel/preset-es2017 together)

- @babel/preset-react: This will add support for react while we bundle our code.

- @babel/preset-stage-2: This will add stage-2 feature of the Ecma TC39 proposal.

- @babel/loader: This is a dependency of Webpack. It allows transpiling Babel using Webpack.

- @babel/core: This is a dependency for the @babel/loader itself.


- html-webpack-plugin: It creates HTML files to serve your bundle file(s).


- style-loader: Adds CSS to the DOM by injecting style tag.

- css-loader: interprets @import and url() like import/require() and will resolve them

- sass-loader: compile SCSS to CSS.

- node-sass: sass-loader required node-sass as a peer dependency

- extract-text-webpack-plugin: moves all the required .css modules into a separate CSS file.

- ptimize-css-assets-webpack-plugin: uglify and minimize all our code to reduce the bundle size, used for prduction evn

- uglifyjs-webpack-plugin:  minimize and optimize CSS code, used for prduction evn


## Babel config file .babelrc
```
{
  "presets": [
    "@babel/env",
    "@babel/preset-react",
    [
      "@babel/preset-stage-2",
      {
        "decoratorsLegacy": true
      }
    ]
  ]
}
```

## Webpack config file 
To support different environments, create config folder and webpack.base.config.js. 
Which contains all of the common features.Changes in this one file will reflect in all environments. 

module.rules define the set of rules that Webpack will apply to certain file extensions.


## webpack-dev-server
```
webpack-dev-server --mode development --config config/webpack.base.config.js --open --hot --history-api-fallback
```
Create script
```
"scripts": {
   "start:dev": "webpack-dev-server --mode development --config config/webpack.base.config.js --open --hot --history-api-fallback"
}
```
- The flag --open tells the webpack-dev-server to open up the browser.

- The flag --hot tells the webpack-dev-server to enable Webpack’s hot module replacement feature. This updates the browser every time you hit ctrl + s

- The flag — -history-api-fallback tells webpack-dev-server to fallback to index.html in the event that a requested resource cannot be found. You can read more about history-api-fallback here.


## Prod evn
```
"scripts": {
    "start:dev": "webpack-dev-server --mode development --config config/webpack.base.config.js --open --hot --history-api-fallback",
    "prestart:prod": "webpack --mode production --config config/webpack.prod.config.js --env.NODE_ENV=production --progress",
    "start:prod": "node server"
  },
```
