Some EsLint rules that I use for my own projects. So I don't have to write them every time.

Unless you want to code like me, nothing to see here, move along.

```sh
npm install --save-dev @schmupu/my-eslint-rules
```

```js
// copy-pastie-me to .eslintrc.json:
{
  "extends": "@schmupu/my-eslint-rules"
}
```

Or maybe:

```sh
npm install --save-dev @schmupu/my-eslint-rules loash.defaultsdeep
```

```js
// copy-pastie-me to .eslintrc.js:
'use strict'

const defaultsDeep = require( 'lodash.defaultsdeep' );

module.exports = defaultsDeep( {
  // project specific rules

  // parser: 'babel-eslint', // probably want this, at least until eslint starts parsing
  // modern js nicely
}, require( '@schmupu/my-eslint-rules' ) )
```

Or even:
```sh
npm install --save-dev @schmupu/my-eslint-rules loash.defaultsdeep eslint-config-react-app
```

```js
// copy-pastie-me to .eslintrc.js:
'use strict'

const defaultsDeep = require( 'lodash.defaultsdeep' );

module.exports = defaultsDeep( {
    // project-specific rules
},
    require( '@schmupu/my-eslint-rules' ),
    require( 'eslint-config-react-app' )
)
```

