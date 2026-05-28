# Distorted IDBFactory.prototype.databases (distorted-idb-factory-databases)

For security `IDBFactory.prototype.databases` is distorted by Lightning Web Security.

<!-- START generated embed: @locker/distortion/src/IDBFactory/docs/databases-value.md -->
## IDBFactory.prototype.databases

The [`IDBFactory.prototype.databases()`](https://developer.mozilla.org/en-US/docs/Web/API/IDBFactory/databases) method returns a promise that resolves to an array of objects containing the name and version of each available IndexedDB database.

This distortion protects `IDBFactory.prototype.databases` and limits the view to databases created from within the sandbox. Databases inside the sandbox are protected from code outside or in other sandboxes.

### Distorted Behavior

The result includes only databases that belong to the sandbox.
<!-- END generated embed, please keep comment -->
