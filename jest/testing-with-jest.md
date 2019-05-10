# Testing with Jest

Jest is a JavaScript unit testing framework from the facebook guys that was primary developed for testing react applications even thought it is not limited to that. It has some pretty cool features like snapshot testing, a watch mode that re-runs tests on file changes and a built-in code coverage report that requires zero configuration.

## Setup

In case you created your project using the `create-react-app` CLI tool you get out of the box Jest support and don't have to manually install the Jest dependendcies. If this is the case just skip this section. In case you are starting out from scratch just read on.

We start by creating a new Node.js project:

```
$ mkdir project
$ cd project
$ npm init -y
```

Next install Jest as a so called dev dependency:

```
$ npm install --save-dev jest
```

and add a test script in your `package.json` similar to the one shown below:

```json
"scripts": {
    "test": "jest"
}
```

In order run Jest simply type:

```
$ npm run test
```

Running this command will show the following output on your shell:
```
$ npm test

> project@1.0.0 test C:\project
> jest

No tests found
In C:\project
  2 files checked.
  testMatch: **/__tests__/**/*.js?(x),**/?(*.)+(spec|test).js?(x) - 0 matches
  testPathIgnorePatterns: \\node_modules\\ - 2 matches
Pattern:  - 0 matches
npm ERR! Test failed.  See above for more details.
```
Congratulations! You just ran Jest. Although it did not test anything since it could not find any test. The next section will show you how to write your first test with Jest.

## Writing your first Jest test

Let's get started by writing a simple calculator in `calculator.js` that can just add two numbers.

```javascript
class Calculator {

    add(a, b) {
        return a + b;
    }

}

module.exports = Calculator;
```

The corresponding test `calculator.test.js` would look like follows:

```javascript
const Calculator = require( './calculator');

test('add', () => {
    const calculator = new Calculator();
    
    expect(calculator.add(4, 2)).toBe(6);
});
```

## Matchers
## Snapshots
## Mock Functions
