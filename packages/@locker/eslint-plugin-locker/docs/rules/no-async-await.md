# Disallow async-await Syntax Usage (no-async-await)

The [async-await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
syntax is  not supported in Lightning Locker. To prevent code from breaking use
the `@locker/rollup-plugin`.

## Rule Details

Example of **incorrect** code:

<!-- eslint-disable-next-line no-unused-vars -->
```js
async function fetchJSON(url) {
    const res = await fetch(url);
    return res.json();
}
```

Example of **correct** code:

<!-- eslint-disable-next-line no-unused-vars -->
```js
function fetchJSON(url) {
    return fetch(url).then(res => res.json());
}
```
