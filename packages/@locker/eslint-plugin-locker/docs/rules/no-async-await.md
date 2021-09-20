# Disallow async-await Syntax Usage (no-async-await)

The [async-await][1] syntax is  not supported in Lightning Locker. To prevent
code from breaking use the [`@locker/rollup-plugin`].

## Rule Details

Example of **incorrect** code:

```js
async function fetchJSON(url) {
    const res = await fetch(url);
    return res.json();
}
```

Example of **correct** code:

```js
function fetchJSON(url) {
    return fetch(url).then((res) => res.json());
}
```

[1]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)
[`@locker/rollup-plugin`]: https://www.npmjs.com/package/@locker/rollup-plugin
