# @locker/eslint-plugin-locker

> Locker Next eslint rules.

## Installation

```bash
$ npm install eslint @locker/eslint-plugin-locker --save-dev
```

## Usage

Add `locker` to the `plugins` section of your configuration. Then configure the
desired rules in the `rules` sections.

Example of `.eslintrc`:

```json
{
    "plugins": ["@locker/eslint-plugin-locker"],
    "rules": {
        "@locker/locker/blocked-element-properties": "error",
        "@locker/locker/no-document-domain-assignment": "error",
        "@locker/locker/null-window-top": "error"
    }
}
```

For more details about configuration please refer to the dedicated section in the ESLint documentation: https://eslint.org/docs/user-guide/configuring

## Configurations

To choose configuration settings, install the [`eslint-config-locker`](https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-config-locker) sharable configuration package.

## Rules

### Locker

| Rule ID                                                                                    | Description                                                       | Fixable |
| ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- | ------- |
| [locker/blocked-document-properties](./docs/rules/blocked-document-properties.md) | disallow blocked Document properties |         |
| [locker/blocked-element-properties](./docs/rules/blocked-element-properties.md) | disallow blocked Element properties |         |
| [locker/blocked-html-element-properties](./docs/rules/blocked-html-element-properties.md) | disallow blocked HTMLElement properties |         |
| [locker/blocked-html-iframe-element-properties](./docs/rules/blocked-html-iframe-element-properties.md) | disallow blocked HTMLIframeElement properties |         |
| [locker/empty-window-location](./docs/rules/empty-window-location.md) | `window.location` is empty |         |
| [locker/no-async-await](./docs/rules/no-async-await.md) | disallow `async await` syntax usage |         |
| [locker/no-document-domain-assignment](./docs/rules/no-document-domain-assignment.md) | disallow `document.domain` assignment |         |
| [locker/no-dynamic-import](./docs/rules/no-dynamic-import.md) | disallow dynamic `import` |         |
| [locker/null-document-location](./docs/rules/null-document-location.md) | `document.location` is 'null' |         |
| [locker/null-shadow-root-host](./docs/rules/null-shadow-root-host.md) | `shadowRoot.host` is 'null' |         |
| [locker/null-window-top](./docs/rules/null-window-top.md) | `window.top` is 'null'                                   | 🔧      |
