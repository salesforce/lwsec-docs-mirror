# Prevent access to document.all (undefined-document-all)

The `document.all` getter returns `undefined` when Lightning Web Security is enabled.

## Rule Details

Example of **incorrect** code:

```js
document.all[0];
```

Example of **correct** code:

```js
if (document.all === undefined) {
    // ...
}
```
