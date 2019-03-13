# eslint-config

[![npm](https://img.shields.io/npm/v/@flynns-devstation/eslint-config.svg?style=for-the-badge)](https://www.npmjs.com/package/@flynns-devstation/eslint-config)

This package provides Flynns Devstation's .eslintrc as an extensible shared config.

## Features

* Supports TypeScript with `@typescript-eslint/eslint-plugin`
* Supports React and React Hooks
* Based on `eslint-config-airbnb-typescript`
* Works together with prettier

## Usage

1. Install config and peerDependencies

```bash
npm i -D @flynns-devstation/eslint-config \
  @typescript-eslint/eslint-plugin \
  eslint \
  eslint-plugin-import \
  eslint-plugin-jsx-a11y \
  eslint-plugin-react \
  eslint-plugin-react-hooks \
  typescript
```

or

```bash
yarn add -D @flynns-devstation/eslint-config \
  @typescript-eslint/eslint-plugin \
  eslint \
  eslint-plugin-import \
  eslint-plugin-jsx-a11y \
  eslint-plugin-react \
  eslint-plugin-react-hooks \
  typescript
```

2. Create eslint config

```js
// .eslintrc.js
module.exports = {
  extends: ['@flynns-devstation'],
}
```

3. Create a `lint` job in your package.json

```json
{
  "scripts": {
    "lint": "eslint --cache --ext .ts,.tsx ./src"
  }
}
```

4. Run `npm run lint` or `yarn lint` to lint all your `ts` and `tsx` files

## Contributing

1. Fork it
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Create new Pull Request

## LICENSE

Copyright (c) 2019-present. See [License](./LICENSE) for details.
