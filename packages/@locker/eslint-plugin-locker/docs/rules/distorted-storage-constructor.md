# Distorted Storage Constructor (distorted-storage-constructor)

For security the `Storage` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Storage/docs/constructor-value.md -->
## Storage API: Storage.prototype

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode. The storage is accessible on the browser and holds its shape across multiple tabs from the same domain. Therefore, we would have to store each namespaces storage in a synthetic storage, where we do not allow malicious users to add, modify, or clear data items in global or from other namespaces.

KEY: The key() method of the Storage interface, when passed a number n, returns the name of the nth key in a given Storage object. The order of keys is user-agent defined, so you should not rely on it. Therefore, it is okay to have the storage items out of order.

### Distorted Behavior

Distorted behaviors from `Storage.prototype`:

* `length`
* `setItem`
* `getItem`
* `key`
* `removeItem`
* `clear`

This distortion prepends an LSKey[NS] to all storage values set in each namespace where NS is the namespace name. This distortion uses a SecureStorage class that implements all methods and properties from the raw Storage. This distoration also uses a proxy to mimic interactibility features that are on the raw Storage. Storage Example:

[Global]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y', 'LSKey[NS1]x': 'y', 'LSKey[NS2]x': 'y' }`

[NS1]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

[NS2]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

The proxy wrap has traps that allow for our Storage to have features that are the same as the raw Storage. Such features include getting, setting, iterating and basic object features.

* Set/Get: `localStorage.x = 'y'; localStorage; // { 'x': 'y' }`
* Define Property: `Object.defineProperty(localStorage, 'foo', { value: 'bar' }); // { 'foo': 'bar', 'x': 'y' }`
* Delete Property: `delete localStorage.foo; // { 'x': 'y' }`
* Iteration: `Object.keys(localStorage); // ['x']`
* Has: `'x' in sessionStorage; localStorage.hasOwnProperty('x'); // true, true`
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/clear-value.md -->
## value: Storage.prototype.clear [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

Since each sandbox uses it's own synthetic storage, we cannot allow a malicious user to clear all the data items in system mode.

### Distorted Behavior

This distortion deletes all data items from its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/getItem-value.md -->
## value: Storage.prototype.getItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion retrieves data items from its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/key-value.md -->
## value: Storage.prototype.key [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

The key() method of the Storage interface, when passed a number n, returns the name of the nth key in a given Storage object. The order of keys is user-agent defined, so you should not rely on it. Therefore, it is okay to have the storage items out of order.

### Distorted Behavior

This distortion retrieves a key value at a specific index from its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/length-getter.md -->
## get: Storage.prototype.length [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to retrieve the storage of another sandbox, we must create a synthetic storage for each sandbox. When looking at length, we must retrieve the number of data items in the synthetic storage rather than the system mode storage.

### Distorted Behavior

This distortion retrieves the number of data items in its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/removeItem-value.md -->
## value: Storage.prototype.removeItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

Since each sandbox uses it's own synthetic storage, we cannot allow a malicious user to clear a data item from another sandbox.

### Distorted Behavior

This distortion deletes a data item from its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/setItem-value.md -->
## value: Storage.prototype.setItem [Main]

### Summary

The Storage interface provides access to the a particular domain's session or local storage. It allows the addition, modification, or deletion of stored data items which is shared in system mode.

In order for one sandbox not to modify the storage of another sandbox, we must create a synthetic storage for each sandbox.

### Distorted Behavior

This distortion adds or modifies data items in its synthetic storage.
<!-- END generated embed please keep comment here to allow auto update -->
