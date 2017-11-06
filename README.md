
# Sourcegraph tsconfig

[![npm](https://img.shields.io/npm/v/@sourcegraph/tsconfig.svg)](https://www.npmjs.com/package/@sourcegraph/tsconfig)
[![downloads](https://img.shields.io/npm/dt/@sourcegraph/tsconfig.svg)](https://www.npmjs.com/package/@sourcegraph/tsconfig)
[![build](https://travis-ci.org/sourcegraph/tsconfig.svg?branch=master)](https://travis-ci.org/sourcegraph/tsconfig)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)

Base tsconfig.json for TypeScript projects at Sourcegraph.
It only includes compiler options that make TypeScript more strict.
It does not set any project-specific or environmental settings.

## Usage

```
npm install --save-dev @sourcegraph/tsconfig
```

Then add this tsconfig.json:

```json
{
  "extends": "./node_modules/@sourcegraph/tsconfig/tsconfig.json"
}
```

## Making changes

```
npm link
cd <project>
npm link @sourcegraph/tsconfig
npm run lint
```

## Publish a new version

Follow [semver](http://semver.org/).

```
npm version major|minor|patch
git push
git push --tags
npm publish
```

