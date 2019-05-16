# Fail to compile jsx in node_modules/.js

## Reproduce
1. cd link-module && yarn link
2. cd demo && yarn link link-module
3. yarn serve

```
Failed to compile.

./node_modules/link-module/index.js 4:6
Module parse failed: Unexpected token (4:6)
You may need an appropriate loader to handle this file type.
|   render () {
|     return (
>       <div>link-jsx in .js</div>
|     )
|   }
```

## It is ok if link .vue
1. modify `"main": "index.js"` to `"main": "index.vue"` in link-module `package.json`

```
{
  "name": "link-module",
  "version": "1.0.0",
  "main": "index.vue",
  "license": "MIT"
}
```

2. yarn serve // no error
