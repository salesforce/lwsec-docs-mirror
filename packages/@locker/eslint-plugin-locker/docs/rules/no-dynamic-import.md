# Disallow Dynamic Import (no-dynamic-import)

Lightning Locker may prohibit
[dynamic import](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/import#Dynamic_Imports).
To prevent code from breaking the `@locker/rollup-plugin` or
[script injection](https://developer.mozilla.org/en-US/docs/Web/API/HTMLScriptElement#Dynamically_importing_scripts)
should be used instead.

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
