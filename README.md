# React Redux Webpack4 Project

## Reference
- How to build your own React boilerplate [highly recommend]
    - https://codeburst.io/how-to-build-your-own-react-boilerplate-1a97d09337fd
    - https://github.com/itzsaga/react-boilerplate-blog

- How to conquer Webpack 4 and build a sweet React app
    - https://medium.freecodecamp.org/how-to-conquer-webpack-4-and-build-a-sweet-react-app-236d721e6745

- How to Create a React app from scratch using Webpack 4
    - https://codeburst.io/how-to-create-a-react-app-from-scratch-using-webpack-4-530b43a81dae    

- How to structure your react app 
    - https://itnext.io/how-to-structure-your-react-app-98c48e102aad

## Features
- Hot reloading using webpack-dev-server
- Adding SCSS and HTML support in your code with webpack
- Adding support for features like try/catch, async/await and rest operator
- Creating a production build — optimized and ready for deployment
- Setting up different environments in your code like stage, demo and production

## Create Project
```
    mkdir  reactscratch
    cd     reactscratch
    npm init // intializing package.json file
    /src
        index.js
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



