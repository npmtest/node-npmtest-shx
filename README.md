# npmtest-shx

#### basic test coverage for  [shx (v0.2.2)](https://github.com/shelljs/shx#readme)  [![npm package](https://img.shields.io/npm/v/npmtest-shx.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-shx) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-shx.svg)](https://travis-ci.org/npmtest/node-npmtest-shx)

#### Portable Shell Commands for Node

[![NPM](https://nodei.co/npm/shx.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/shx)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-shx/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-shx/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-shx/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-shx/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-shx/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-shx/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-shx/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-shx/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-shx/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-shx/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-shx/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-shx/build/test-report.html](https://npmtest.github.io/node-npmtest-shx/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-shx/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-shx/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-shx/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-shx/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-shx/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-shx/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-shx/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-shx/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "shx",
    "version": "0.2.2",
    "description": "Portable Shell Commands for Node",
    "bin": {
        "shx": "lib/cli.js"
    },
    "files": [
        "lib"
    ],
    "scripts": {
        "prebuild": "rimraf lib",
        "build": "babel src -d lib",
        "build:watch": "npm run build -- -w",
        "dev": "concurrently -rk 'npm run build:watch' 'npm run lint:watch'",
        "lint": "eslint .",
        "lint:fix": "npm run lint --silent -- --fix",
        "lint:watch": "watch 'npm run lint --silent' src test",
        "prepublish": "npm run build",
        "posttest": "npm run lint --silent",
        "release:major": "shelljs-release major",
        "release:minor": "shelljs-release minor",
        "release:patch": "shelljs-release patch",
        "changelog": "shelljs-changelog",
        "codecov": "codecov",
        "test": "nyc --reporter=text --reporter=lcov mocha",
        "test:watch": "concurrently -rk 'npm run test --silent -- -w' 'npm run lint:watch'"
    },
    "repository": {
        "type": "git",
        "url": "git+https://github.com/shelljs/shx.git"
    },
    "keywords": [
        "shelljs",
        "shell",
        "unix",
        "bash",
        "sh",
        "exec",
        "cli",
        "zsh"
    ],
    "contributors": [
        "Ari Porad <ari@ariporad.com> (http://ariporad.com/)",
        "Levi Thomason <me@levithomason.com> (https://github.com/levithomason)",
        "Nate Fischer <ntfschr@gmail.com>"
    ],
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/shelljs/shx/issues"
    },
    "homepage": "https://github.com/shelljs/shx#readme",
    "devDependencies": {
        "babel-cli": "^6.6.5",
        "babel-preset-es2015": "^6.6.0",
        "babel-register": "^6.7.2",
        "codecov": "^1.0.1",
        "concurrently": "^2.1.0",
        "eslint": "^2.10.1",
        "eslint-config-airbnb-base": "^3.0.1",
        "eslint-plugin-import": "^1.8.0",
        "mocha": "^2.4.5",
        "nyc": "^6.4.0",
        "rimraf": "^2.5.2",
        "shelljs-changelog": "^0.2.0",
        "shelljs-plugin-open": "^0.1.1",
        "shelljs-release": "^0.2.0",
        "should": "^11.1.1",
        "watch": "^0.18.0"
    },
    "dependencies": {
        "es6-object-assign": "^1.0.3",
        "minimist": "^1.2.0",
        "shelljs": "^0.7.3"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
