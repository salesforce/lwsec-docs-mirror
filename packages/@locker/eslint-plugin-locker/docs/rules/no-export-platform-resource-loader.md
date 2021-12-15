# Disallow export from lightning/platformResourceLoader (no-export-platform-resource-loader)

Lightning Web Security does not support exporting directly from the `lightning/platformResourceLoader` module.

## Rule Details

Example of **incorrect** code:

```js
export { loadScript } from 'lightning/platformResourceLoader';
```

Example of **correct** code:

```js
import { loadScript } from 'lightning/platformResourceLoader';
export { loadScript };
```
