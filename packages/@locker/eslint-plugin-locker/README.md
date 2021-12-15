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
        "@locker/locker/blocked-document-properties": "error",
        "@locker/locker/distorted-document-cookie": "warn"
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

| Rule ID | Description | Fixable Using |
| --- | --- | --- |
| [@locker/locker/distorted-cookie-store-properties] | distorted CookieStore properties |   |
| [@locker/locker/distorted-custom-element-registry-properties] | distorted CustomElementRegistry properties |   |
| [@locker/locker/distorted-document-blocked-properties] | disallow blocked Document properties |   |
| [@locker/locker/distorted-document-cookie] | distorted document.cookie |   |
| [@locker/locker/distorted-document-domain-setter] | distort Document#domain setter |   |
| [@locker/locker/distorted-document-exec-command] | distorted document.execCommand |   |
| [@locker/locker/distorted-element-attach-shadow] | distorted Element#attachShadow |   |
| [@locker/locker/distorted-element-attributes-getter] | distort Element#attributes getter |   |
| [@locker/locker/distorted-element-blocked-properties] | disallow blocked Element properties |   |
| [@locker/locker/distorted-element-inner-html-setter] | distort Element#innerHTML setter |   |
| [@locker/locker/distorted-element-insert-adjacent-html] | distort Element#insertAdjacentHTML |   |
| [@locker/locker/distorted-element-outer-html-setter] | distort Element#outerHTML setter |   |
| [@locker/locker/distorted-element-set-attribute] | distort Element#setAttribute APIs |   |
| [@locker/locker/distorted-element-shadow-root-getter] | distort Element#shadowRoot getter |   |
| [@locker/locker/distorted-html-frame-iframe-object-element-content-document-getter] | distort HTML{Frame|IFrame|Object}Element#contentDocument getter |   |
| [@locker/locker/distorted-html-frame-iframe-object-element-content-window-getter] | distort HTML{Frame|IFrame|Object}Element#contentWindow getter |   |
| [@locker/locker/distorted-html-element-blocked-properties] | disallow blocked HTMLElement properties |   |
| [@locker/locker/distorted-html-element-inner-text-setter] | distort HTMLElement#innerText setter |   |
| [@locker/locker/distorted-html-element-outer-text-setter] | distort HTMLElement#outerText setter |   |
| [@locker/locker/distorted-html-element-style-getter] | distort HTMLElement#style getter |   |
| [@locker/locker/distorted-html-embed-object-element-blocked-properties] | disallow blocked HTML{Embed|Object}Element properties |   |
| [@locker/locker/distorted-html-iframe-element-blocked-properties] | disallow blocked HTMLIFrameElement properties |   |
| [@locker/locker/distorted-html-iframe-script-element-src-setter] | distort HTML{IFrame|Script}Element#src setter |   |
| [@locker/locker/distorted-html-link-element-rel-list-setter] | distort HTMLLinkElement#relList setter |   |
| [@locker/locker/distorted-html-link-element-rel-setter] | distort HTMLLinkElement#rel setter |   |
| [@locker/locker/distorted-message-event-source-getter] | distort MessageEvent#source getter |   |
| [@locker/locker/distorted-named-node-map-set-named-item] | distorted NamedNodeMap#setNamedItem |   |
| [@locker/locker/distorted-navigator-service-worker-getter] | distorted Navigator#serviceWorker getter |   |
| [@locker/locker/distorted-node-text-content-setter] | distort Node#textContent setter |   |
| [@locker/locker/distorted-range-create-contextual-fragment] | distorted Range#createContextualFragment |   |
| [@locker/locker/distorted-shadow-root-mode-getter] | distorted ShadowRoot#mode getter |   |
| [@locker/locker/distorted-shared-worker-constructor] | distorted SharedWorker constructor |   |
| [@locker/locker/distorted-storage-constructor] | distorted Storage constructor |   |
| [@locker/locker/distorted-url-create-object-url] | distorted URL.createObjectURL |   |
| [@locker/locker/distorted-window-fetch] | distorted window.fetch |   |
| [@locker/locker/distorted-window-frames-getter] | distorted window.frames getter |   |
| [@locker/locker/distorted-window-opener-getter] | distorted window.opener getter |   |
| [@locker/locker/distorted-window-parent-getter] | distorted window.parent getter |   |
| [@locker/locker/distorted-window-set-interval] | distorted window.setInterval |   |
| [@locker/locker/distorted-window-set-timeout] | distorted window.setTimeout |   |
| [@locker/locker/distorted-worker-constructor] | distorted Worker constructor |   |
| [@locker/locker/distorted-xml-http-request-window-open] | distorted {XMLHttpRequest|Window}#open |   |
| [@locker/locker/no-export-platform-resource-loader] | disallow export from 'lightning/platformResourceLoader' |   |
| [@locker/locker/uncompiled-empty-window-location] | window.location is empty | [`@locker/rollup-plugin`]  |
| [@locker/locker/uncompiled-no-async-await] | disallow 'async await' syntax usage | [`@locker/rollup-plugin`]  |
| [@locker/locker/uncompiled-no-dynamic-import] | disallow dynamic 'import' | [`@locker/rollup-plugin`]  |
| [@locker/locker/uncompiled-null-document-location] | document.location is null | [`@locker/rollup-plugin`]  |
| [@locker/locker/uncompiled-null-window-top] | window.top is null | `--fix` or [`@locker/rollup-plugin`]  |
| [@locker/locker/undefined-document-all] | document.all is undefined |   |

[`@locker/rollup-plugin`]:
https://www.npmjs.com/package/@locker/rollup-plugin
[`@locker/eslint-config-locker`]:
https://www.npmjs.com/package/@locker/eslint-config-locker
[ESLint]:
https://eslint.org/
[`--fix`]:
https://eslint.org/docs/user-guide/command-line-interface#-fix
[@locker/locker/distorted-cookie-store-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-cookie-store-properties.md
[@locker/locker/distorted-custom-element-registry-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-custom-element-registry-properties.md
[@locker/locker/distorted-document-blocked-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-document-blocked-properties.md
[@locker/locker/distorted-document-cookie]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-document-cookie.md
[@locker/locker/distorted-document-domain-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-document-domain-setter.md
[@locker/locker/distorted-document-exec-command]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-document-exec-command.md
[@locker/locker/distorted-element-attach-shadow]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-attach-shadow.md
[@locker/locker/distorted-element-attributes-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-attributes-getter.md
[@locker/locker/distorted-element-blocked-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-blocked-properties.md
[@locker/locker/distorted-element-inner-html-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-inner-html-setter.md
[@locker/locker/distorted-element-insert-adjacent-html]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-insert-adjacent-html.md
[@locker/locker/distorted-element-outer-html-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-outer-html-setter.md
[@locker/locker/distorted-element-set-attribute]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-set-attribute.md
[@locker/locker/distorted-element-shadow-root-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-element-shadow-root-getter.md
[@locker/locker/distorted-html-frame-iframe-object-element-content-document-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-frame-iframe-object-element-content-document-getter.md
[@locker/locker/distorted-html-frame-iframe-object-element-content-window-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-frame-iframe-object-element-content-window-getter.md
[@locker/locker/distorted-html-element-blocked-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-element-blocked-properties.md
[@locker/locker/distorted-html-element-inner-text-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-element-inner-text-setter.md
[@locker/locker/distorted-html-element-outer-text-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-element-outer-text-setter.md
[@locker/locker/distorted-html-element-style-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-element-style-getter.md
[@locker/locker/distorted-html-embed-object-element-blocked-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-embed-object-element-blocked-properties.md
[@locker/locker/distorted-html-iframe-element-blocked-properties]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-iframe-element-blocked-properties.md
[@locker/locker/distorted-html-iframe-script-element-src-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-iframe-script-element-src-setter.md
[@locker/locker/distorted-html-link-element-rel-list-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-link-element-rel-list-setter.md
[@locker/locker/distorted-html-link-element-rel-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-html-link-element-rel-setter.md
[@locker/locker/distorted-message-event-source-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-message-event-source-getter.md
[@locker/locker/distorted-named-node-map-set-named-item]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-named-node-map-set-named-item.md
[@locker/locker/distorted-navigator-service-worker-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-navigator-service-worker-getter.md
[@locker/locker/distorted-node-text-content-setter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-node-text-content-setter.md
[@locker/locker/distorted-range-create-contextual-fragment]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-range-create-contextual-fragment.md
[@locker/locker/distorted-shadow-root-mode-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-shadow-root-mode-getter.md
[@locker/locker/distorted-shared-worker-constructor]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-shared-worker-constructor.md
[@locker/locker/distorted-storage-constructor]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-storage-constructor.md
[@locker/locker/distorted-url-create-object-url]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-url-create-object-url.md
[@locker/locker/distorted-window-fetch]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-fetch.md
[@locker/locker/distorted-window-frames-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-frames-getter.md
[@locker/locker/distorted-window-opener-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-opener-getter.md
[@locker/locker/distorted-window-parent-getter]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-parent-getter.md
[@locker/locker/distorted-window-set-interval]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-set-interval.md
[@locker/locker/distorted-window-set-timeout]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-window-set-timeout.md
[@locker/locker/distorted-worker-constructor]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-worker-constructor.md
[@locker/locker/distorted-xml-http-request-window-open]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/distorted-xml-http-request-window-open.md
[@locker/locker/no-export-platform-resource-loader]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/no-export-platform-resource-loader.md
[@locker/locker/uncompiled-empty-window-location]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/uncompiled-empty-window-location.md
[@locker/locker/uncompiled-no-async-await]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/uncompiled-no-async-await.md
[@locker/locker/uncompiled-no-dynamic-import]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/uncompiled-no-dynamic-import.md
[@locker/locker/uncompiled-null-document-location]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/uncompiled-null-document-location.md
[@locker/locker/uncompiled-null-window-top]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/uncompiled-null-window-top.md
[@locker/locker/undefined-document-all]:
https://github.com/salesforce/lwsec-docs-mirror/blob/v0.14.4/packages/%40locker/eslint-plugin-locker/docs/rules/undefined-document-all.md

