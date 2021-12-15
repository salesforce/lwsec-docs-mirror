# Prevent access to certain HTML{Embed|Object}Element properties (distorted-html-embed-object-element-blocked-properties)

The following `HTML{Embed|Object}Element` properties are prohibited when Lightning Web Security is enabled:
-   getSVGDocument

## Rule Details

Example of **incorrect** code:

```js
embed.getSVGDocument();
```
