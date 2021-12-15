# Disallow Dynamic Import (no-dynamic-import)

Lightning Locker may prohibit [dynamic import][1]. To prevent code from breaking
the [`@locker/rollup-plugin`] or [script injection][2] should be used instead.

## Rule Details

Example of **incorrect** code:

```js
import('./a.js');
```

Example of **correct** code:

```js
const newScript = document.createElement('script');
document.head.appendChild(newScript);
newScript.src = './example.js';
```

[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import#Dynamic_Imports
[2]: https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement#Dynamically_importing_scripts
[`@locker/rollup-plugin`]: https://www.npmjs.com/package/@locker/rollup-plugin
