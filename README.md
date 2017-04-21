# npmtest-csshint

#### basic test coverage for  csshint (v0.3.3)  [![npm package](https://img.shields.io/npm/v/npmtest-csshint.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-csshint) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-csshint.svg)](https://travis-ci.org/npmtest/node-npmtest-csshint)

#### lint your css code

[![NPM](https://nodei.co/npm/csshint.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/csshint)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-csshint/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-csshint/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-csshint/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-csshint/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-csshint/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-csshint/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-csshint/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-csshint/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-csshint/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-csshint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-csshint/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-csshint/build/test-report.html](https://npmtest.github.io/node-npmtest-csshint/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-csshint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-csshint/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-csshint/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-csshint/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-csshint/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-csshint/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-csshint/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-csshint/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "csshint",
    "description": "lint your css code",
    "version": "0.3.3",
    "keywords": [
        "csslint",
        "csshint"
    ],
    "maintainers": [
        {
            "name": "ielgnaw"
        }
    ],
    "dependencies": {
        "chalk": "^1.1.3",
        "edp-core": "^1.0.32",
        "js-yaml": "^3.6.1",
        "manis": "^0.3.0",
        "object-assign": "^4.1.0",
        "postcss": "^5.2.0",
        "strip-json-comments": "^2.0.1"
    },
    "engines": {
        "node": ">=0.10"
    },
    "devDependencies": {
        "babel-cli": "^6.14.0",
        "babel-core": "^6.14.0",
        "babel-istanbul": "^0.11.0",
        "babel-node-debug": "^2.0.0",
        "babel-preset-es2015": "^6.14.0",
        "babel-preset-stage-2": "^6.13.0",
        "chai": "^3.5.0",
        "coveralls": "^2.11.13",
        "debug": "^2.2.0",
        "fecs": "^0.8.7",
        "istanbul": "^0.3.2",
        "jasmine-node": "^1.14.5",
        "json-stringify-safe": "^5.0.1",
        "mocha": "^3.0.2"
    },
    "scripts": {
        "lint": "fecs src test/**/*.spec.js --type=js",
        "compile": "rm -rf lib && ./node_modules/.bin/babel src -d lib --source-maps inline --copy-files",
        "debug": "npm run compile && ./node_modules/.bin/babel-node-debug lib/index.js",
        "test": "npm run compile && ./node_modules/.bin/_mocha --compilers js:babel-core/register --recursive",
        "coverage": "npm run compile && ./node_modules/.bin/babel-node ./node_modules/.bin/babel-istanbul cover _mocha 'test/**/*.spec.@(js|es|es6)'",
        "coverage1": "npm run compile && ./node_modules/.bin/babel-node ./node_modules/.bin/babel-istanbul cover _mocha -- --recursive",
        "coveralls": "cat ./coverage/lcov.info | coveralls",
        "sourcemap": "./node_modules/.bin/babel src -d lib -s",
        "watch": "./node_modules/.bin/babel -w src -d lib --source-maps inline --copy-files",
        "prepublish": "npm run compile"
    },
    "main": "./lib/checker.js",
    "bin": {
        "csshint": "./bin/csshint-cli"
    },
    "repository": {
        "type": "git",
        "url": "git@github.com:ecomfe/node-csshint"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
