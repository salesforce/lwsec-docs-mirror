# distorted-promise-try

Disallow `Promise.try` with `eval`.

## Rule Details

This rule disallows the use of `Promise.try` with `eval` which is distorted by Lightning Web Security. Regular `Promise.try` usage with functions is allowed.

Examples of **incorrect** code for this rule:

```js
Promise.try(eval);

Promise.try(eval, 'some code');
```

Examples of **correct** code for this rule:

```js
Promise.try(() => {
    return someAsyncOperation();
});

Promise.try(async () => {
    return await fetch('/api/data');
});

Promise.try(function() {
    return someValue;
});
```

## When Not To Use It

If you are not using Lightning Web Security, you can disable this rule.
