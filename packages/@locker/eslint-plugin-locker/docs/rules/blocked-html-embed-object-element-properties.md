# Disallow Blocked HTML{Embed|Object}Element Properties (blocked-html-embed-object-element-properties)

For security the following `HTML{Embed|Object}Element` properties are prohibited
in Lightning Locker:
-   getSVGDocument

## Rule Details

Example of **incorrect** code:

```js
embed.getSVGDocument();
```
