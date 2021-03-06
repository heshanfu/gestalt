# Gestalt
[![Build status](https://badge.buildkite.com/2c6b6e9f79054095354cc061876e4885f4b9212e1dbebda270.svg?branch=master)](https://buildkite.com/pinterest/gestalt)
[![NPM Version](https://img.shields.io/npm/v/gestalt.svg)](https://www.npmjs.com/package/gestalt)

Gestalt is a set of React UI components that enforces Pinterest’s design language. We use it to streamline communication between designers and developers by enforcing a bunch of fundamental UI components. This common set of components helps raise the bar for UX & accessibility across Pinterest.

[View the full docs](https://pinterest.github.io/gestalt)
or
[Check out the Gestalt playground](https://codesandbox.io/s/k5plvp9v8v)


## Usage

Gestalt exports each component as ES6 modules and a single, precompiled CSS file:

```js
import { Text } from 'gestalt';
import 'gestalt/dist/gestalt.css';
```

That syntax is Webpack specific (and will work with Create React App), but you can use Gestalt anywhere that supports ES6 module bundling and global CSS.

## Development

Install dependencies.

```bash
yarn
```

Start the development server:

```bash
yarn start
open "http://localhost:8080"
```
Visit [http://localhost:8080/](http://localhost:8080) and click on a component to view the docs.

Running Jest unit tests:

```bash
yarn test
```

Using the Masonry playground:

```bash
cd test && yarn start
open "http://localhost:3000"
```

Running Masonry's integration tests. This will likely leave hanging Firefox processes left over, so please be warned.

```bash
./run_integration_tests
```

## Releasing

The following outlines our release process:

* Checkout a new branch.
* Bump package version in `package.json`.
* Open a pull request with the new version and land that in master.
* Once the version is bumped in master, checkout that commit locally.
* Publish the tag, npm package, and docs with: `./scripts/publish.js`.
* Draft a release from the tag and update the release notes at https://github.com/pinterest/gestalt/releases
