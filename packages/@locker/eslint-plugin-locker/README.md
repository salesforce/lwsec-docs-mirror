# @locker/eslint-plugin-locker

> Locker [ESLint] rules

## Installation

```shell
$ yarn add --dev eslint @locker/eslint-plugin-locker
```

## Usage

Add `@locker/eslint-plugin-locker` to the `plugins` section of your configuration.
Then configure the desired rules in the `rules` section.

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

For more details about configuration please refer to the dedicated section in
the ESLint documentation:<br>
https://eslint.org/docs/user-guide/configuring

## Configurations

To choose configuration settings, install the [`@locker/eslint-config-locker`]
sharable configuration package.

## Rules

### Locker

| Rule ID                                                                                    | Description                                                       | Fixable |
| ------------------------------------------------------------------------------------------ | ----------------------------------------------------------------- | ------- |
| [@locker/locker/blocked-document-properties] | disallow blocked Document properties |         |
| [@locker/locker/blocked-element-properties] | disallow blocked Element properties |         |
| [@locker/locker/blocked-html-element-properties] | disallow blocked HTMLElement properties |         |
| [@locker/locker/blocked-html-iframe-element-properties] | disallow blocked HTMLIframeElement properties |         |
| [@locker/locker/empty-window-location] | `window.location` is empty |         |
| [@locker/locker/no-async-await] | disallow `async await` syntax usage |         |
| [@locker/locker/no-document-domain-assignment] | disallow `document.domain` assignment |         |
| [@locker/locker/no-dynamic-import] | disallow dynamic `import` |         |
| [@locker/locker/no-import-platform-resource-loader] | disallow `import` or `export` from `'lightning/platformResourceLoader'`|         |
| [@locker/locker/null-document-location] | `document.location` is `'null'` |         |
| [@locker/locker/null-shadow-root-host] | `shadowRoot.host` is `'null'` |         |
| [@locker/locker/null-window-top] | `window.top` is `'null' `                                  | 🔧      |

[`@locker/eslint-config-locker`]:
https://www.npmjs.com/package/@locker/eslint-config-locker
[@locker/locker/blocked-document-properties]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/blocked-document-properties.md
[@locker/locker/blocked-element-properties]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/blocked-element-properties.md
[@locker/locker/blocked-html-element-properties]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/blocked-html-element-properties.md
[@locker/locker/blocked-html-iframe-element-properties]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/blocked-html-iframe-element-properties.md
[@locker/locker/empty-window-location]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/empty-window-location.md
[@locker/locker/no-async-await]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/no-async-await.md
[@locker/locker/no-document-domain-assignment]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/no-document-domain-assignment.md
[@locker/locker/no-dynamic-import]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/no-dynamic-import.md
[@locker/locker/no-import-platform-resource-loader]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/no-import-platform-resource-loader.md
[@locker/locker/null-document-location]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/null-document-location.md
[@locker/locker/null-shadow-root-host]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/null-shadow-root-host.md
[@locker/locker/null-window-top]:
https://github.com/salesforce/locker/tree/master/packages/%40locker/eslint-plugin-locker/docs/rules/null-window-top.md
[ESLint]:
https://eslint.org/
