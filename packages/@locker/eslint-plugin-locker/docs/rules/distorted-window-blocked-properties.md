# Prevent access to certain Window properties (distorted-window-blocked-properties)

The following `Window` properties are prohibited when Lightning Web Security is enabled:
-   find

## Rule Details

Example of **incorrect** code:

```js
window.find('foo');
```
