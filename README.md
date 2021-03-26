## ⚠️ Disclaimer! The @island.is/ui library is not officially release and is only available as an alpha version at the moment. We are going to improve it and provide a better support in the future. Proceed with cautious, things might break.

## Setup

1. Create a new next app

```bash
npx create-next-app
```

2. Set up TypeScript

```bash
touch tsconfig.json
yarn add --dev typescript @types/react @types/node
```

3. Install `@island.is/ui`

```bash
yarn add @island.is/ui -E
```

Install its required peerDependencies

```bash
yarn add @rehooks/component-size animejs classnames date-fns downshift hypher lodash markdown-to-jsx react react-animate-height react-datepicker react-dropzone react-keyed-flatten-children react-select react-toastify react-use reakit treat@1.6.0 -E
```

> Make sure to install `treat@1.6.0`. It won't work with treat@2.

4. Configure `next.config.js`

We need to use specific versions of `webpack` and `next` that are supported by Treat.

```bash
yarn add next@10.0.1 -E
yarn add webpack@4.44.1 next-treat next-transpile-modules -DE
```

Create a `next.config.js` at the root of the project and add the following.

```javascript
const withTreat = require('next-treat')();
const withTM = require('next-transpile-modules')(['@island.is/ui']);

module.exports = withTreat(withTM());
```

5. Run the development server

```bash
yarn dev
```

You can now open `http://localhost:3000`

6. Voilà!

![preview](https://user-images.githubusercontent.com/937328/112627694-d7304400-8e29-11eb-8cac-1f5a6aab7cac.jpg)
