## Steup

### Project

1. Install `Node 14`
2. npm init
3. npm i -g near-cli
4. npm i --save-dev 'assemblyscript@^0.19.3'
5. npx asinit .
6. npm i --save-dev @as-pect/cli
7. npx asp --init
8. npm i near-sdk-as

### Modification

1. update `as-pect.config.js` and import `near-sdk-as/imports`
2. replace asconfig.json content by
```js
{
  "entry": "assembly/index.ts",
  "options": {
    "binaryFile": "out/main.wasm"
  },
  "extends": "near-sdk-as/asconfig.json"
}
``` 
3. Delete `tests` folder
4. Add out folder.
5. Import near-sdk-as types: add a new file `assembly/as_types.d.ts` then copy/past this code
```js
/// <reference types="near-sdk-as/assembly/as_types" />
```

