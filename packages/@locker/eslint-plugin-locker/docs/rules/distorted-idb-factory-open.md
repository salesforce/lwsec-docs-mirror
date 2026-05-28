# Distorted IDBFactory.prototype.open (distorted-idb-factory-open)

For security `IDBFactory.prototype.open` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/IDBFactory/docs/open-value.md -->
## IDBFactory.prototype.open

The [`IDBFactory.prototype.open()`](https://developer.mozilla.org/en-US/docs/Web/API/IDBFactory/open) method requests opening a connection to an IndexedDB database.

This distortion protects `IDBFactory.prototype.open` by namespacing database names to the sandbox. Databases inside the sandbox are isolated from databases outside or in other sandboxes.

### Distorted Behavior

The opened database belongs only to the sandbox.
<!-- END generated embed, please keep comment -->
