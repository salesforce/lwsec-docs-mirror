# Undefined document.all (undefined-document-all)

The value of `document.all` in Lightning Locker is `undefined`. This isn’t
likely to break code but is something to be aware of.

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
