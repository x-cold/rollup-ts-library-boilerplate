Rollup Ts Library Boilerplate
---

[![NPM version][npm-image]][npm-url]
[![build status][gitflow-image]][gitflow-url]
[![Test coverage][codecov-image]][codecov-url]
[![npm download][download-image]][download-url]

[npm-image]: https://img.shields.io/npm/v/rollup-ts-library-boilerplate.svg?style=flat-square
[npm-url]: https://npmjs.org/package/rollup-ts-library-boilerplate
[gitflow-image]: https://github.com/x-cold/rollup-ts-library-boilerplate/actions/workflows/test.yml/badge.svg?branch=master
[gitflow-url]: https://github.com/x-cold/rollup-ts-library-boilerplate/actions/workflows/test.yml
[codecov-image]: https://codecov.io/gh/x-cold/rollup-ts-library-boilerplate/branch/master/graph/badge.svg
[codecov-url]: https://codecov.io/gh/x-cold/rollup-ts-library-boilerplate
[download-image]: https://badgen.net/npmnpm/dt/rollup-ts-library-boilerplate
[download-url]: https://npmjs.org/package/rollup-ts-library-boilerplate

A starter project that makes creating a TypeScript library extremely easy.

### Usage

> The version of your node.js should be greater than v12

```bash
git clone git@github.com:x-cold/rollup-ts-library-boilerplate.git YOURFOLDERNAME
cd YOURFOLDERNAME

# Run npm install and write your library name when asked. That's all!
npm install
```

### Features

 - Zero-setup. After running `npm install` things will setup for you :wink:
 - **[RollupJS](https://rollupjs.org/)** for multiple optimized bundles following the [standard convention](http://2ality.com/2017/04/setting-up-multi-platform-packages.html) and [Tree-shaking](https://alexjoverm.github.io/2017/03/06/Tree-shaking-with-Webpack-2-TypeScript-and-Babel/)
 - Tests, coverage and interactive watch mode using **[Jest](http://facebook.github.io/jest/)**
 - **Docs automatic generation and deployment** to `gh-pages`, using **[TypeDoc](http://typedoc.org/)**
 - Automatic types `(*.d.ts)` file generation
 - (Optional) **Automatic releases and changelog**, using [standard-version](https://github.com/conventional-changelog/standard-version#readme), [Commitizen](https://github.com/commitizen/cz-cli), [Conventional changelog](https://github.com/conventional-changelog/conventional-changelog) and [Husky](https://github.com/typicode/husky) (for the git hooks)
 - Deploy your docs to github pages via gh-pages branch

### Importing library

You can import the generated bundle to use the whole library generated by this starter:

```javascript
import myLib from 'mylib'
```

Additionally, you can import the transpiled modules from `dist/lib` in case you have a modular library:

```javascript
import something from 'mylib/dist/lib/something'
```

### NPM scripts

 - `npm lint`: Eslint code
 - `npm lint:fix`: Eslint code and try to fix problems
 - `npm start`: Realtime complie code
 - `npm run docs`: Generate type documents
 - `npm run build`: Build ths dist products
 - `npm run release`: The same as `npm run release:patch`
 - `npm run release:patch`: Automatically upgrade patch versioin and update CHANGELOG.md
 - `npm run release:minor`: Automatically upgrade minor versioin and update CHANGELOG.md
 - `npm run release:major`: Automatically upgrade major versioin and update CHANGELOG.md
 - `npm run test`: Run test suite via jest with code coverage
 - `npm run test:watch`: Run test suite in [interactive watch mode](http://facebook.github.io/jest/docs/cli.html#watch)
 - `npm run test:prod`: Run linting and generate coverage
 - `npm run deploy`: Clean docs directory and rebuild docs pages

### Git Hooks

There is already set a `precommit` hook for formatting your code with Eslint and Commitlint :nail_care:

By default, there are two disabled git hooks. They're set up when you run the `npm i` script. They make sure:
 - You follow a [conventional commit message](https://github.com/conventional-changelog/conventional-changelog)
