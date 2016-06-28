This repository demonstrate a simple coverage example using:
- [mochajs/mocha](https://github.com/mochajs/mocha) and [istanbuljs/nyc](https://github.com/istanbuljs/nyc)
- [facebook/jest](https://github.com/facebook/jest)

The jest example is failing at coverage report.

Linked issue: https://github.com/facebook/jest/issues/1214.

```sh
git clone git@github.com:vvo/test-coverage-jest.git
cd test-coverage-jest
npm install
npm test

> test-coverage-jest@1.0.0 test /home/vvo/Dev/Algolia/test-coverage
> npm run test:mocha && npm run test:jest


> test-coverage-jest@1.0.0 test:mocha /home/vvo/Dev/Algolia/test-coverage
> NODE_ENV=test nyc mocha --compilers js:babel-register



  test
    ✓ works


  1 passing (345ms)

----------------|----------|----------|----------|----------|----------------|
File            |  % Stmts | % Branch |  % Funcs |  % Lines |Uncovered Lines |
----------------|----------|----------|----------|----------|----------------|
 test-coverage/ |      100 |      100 |      100 |      100 |                |
  index.js      |      100 |      100 |      100 |      100 |                |
----------------|----------|----------|----------|----------|----------------|
All files       |      100 |      100 |      100 |      100 |                |
----------------|----------|----------|----------|----------|----------------|


> test-coverage-jest@1.0.0 test:jest /home/vvo/Dev/Algolia/test-coverage
> jest --no-cache --coverage

Using Jest CLI v13.0.0, jasmine2
 PASS  __tests__/index.js (0.093s)
1 test passed (1 total in 1 test suite, run time 0.601s)
----------------|----------|----------|----------|----------|----------------|
File            |  % Stmts | % Branch |  % Funcs |  % Lines |Uncovered Lines |
----------------|----------|----------|----------|----------|----------------|
 test-coverage/ |       50 |      100 |        0 |       50 |                |
  index.js      |       50 |      100 |        0 |       50 |              2 |
----------------|----------|----------|----------|----------|----------------|
All files       |       50 |      100 |        0 |       50 |                |
----------------|----------|----------|----------|----------|----------------|
```
