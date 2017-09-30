
# Sourcegraph tsconfig

[![Version](https://img.shields.io/npm/v/@sourcegraph/tsconfig.svg)](https://www.npmjs.com/package/@sourcegraph/tsconfig)
[![Downloads](https://img.shields.io/npm/dt/@sourcegraph/tsconfig.svg)](https://www.npmjs.com/package/@sourcegraph/tsconfig)

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
  "extends": "@sourcegraph/tsconfig"
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

