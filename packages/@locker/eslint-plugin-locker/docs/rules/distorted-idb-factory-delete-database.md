# Distorted IDBFactory.prototype.deleteDatabase (distorted-idb-factory-delete-database)

For security `IDBFactory.prototype.deleteDatabase` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/IDBFactory/docs/deleteDatabase-value.md -->
## IDBFactory.prototype.deleteDatabase

The [`IDBFactory.prototype.deleteDatabase()`](https://developer.mozilla.org/en-US/docs/Web/API/IDBFactory/deleteDatabase) method requests the deletion of an IndexedDB database.

This distortion protects `IDBFactory.prototype.deleteDatabase` by namespacing database names to the sandbox. Sandboxed code can only delete databases that belong to its own sandbox.

### Distorted Behavior

Only databases that belong to the sandbox can be deleted.
<!-- END generated embed, please keep comment -->
