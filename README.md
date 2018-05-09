# React Redux Webpack4 Project

## Reference
- How to Create a React app from scratch using Webpack 4
    - https://codeburst.io/how-to-create-a-react-app-from-scratch-using-webpack-4-530b43a81dae    
- How to structure your react app 
    - https://itnext.io/how-to-structure-your-react-app-98c48e102aad

## Create Project
```
    mkdir  reactscratch
    cd     reactscratch
    npm init // intializing package.json file
```

## Project structure
Divide components to bundle by business value 
- Common bundle: Keeps all common components, like Header, Footer, Button, Modal and etc.
- User bundle: have all the components specific to a user

Every bundle has a few folders:
- actionCreators hold redux-actions
- components
    - Header
        - Header.js
        - HeaderContainer.js # getting data from redux-store/relay, define actions, injecting intl or jss
        - index.js
- reducers is a folder for all the reducers for a bundle
- routes keeps all the routes for the current bundle

## Support ES 6
- dependencies
- .babelrc config file


## webpack.config.js


