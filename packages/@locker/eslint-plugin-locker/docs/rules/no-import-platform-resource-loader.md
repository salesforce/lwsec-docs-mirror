# Disallow Import from 'lightning/platformResourceLoader' (no-import-platform-resource-loader)

Lightning Locker prohibits any kind of `import` or `export` from the `'lightning/platformResourceLoader'` module.

## Rule Details

Example of **incorrect** code:

```js
import { loadScript } from 'lightning/platformResourceLoader';
loadScript(this, './some.js');
```

Example of **correct** code:

```js
const newScript = document.createElement('script');
document.head.appendChild(newScript);
newScript.src = './some.js';
```
