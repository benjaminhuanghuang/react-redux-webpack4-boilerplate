## Dependencies
```
    npm i ject enzyme enzyme-adapter-react-16 react-test-render -D
```


## Jest setup
/test/enzyme.setup.js
```
    import Enzyme from 'enzyme'
    import Adapter from 'enzyme-adapter-react-16'

    Enzyme.configure({
        adapter: new Adapter()
    })
```
package.json
```
    "jest": {
        "setupTestFrameworkScriptFile": "./test/enzyme.setup.js"
    },
```
## Test script
```
    "test: "jest ./test"
```