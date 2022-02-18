# Distorted Storage Constructor (distorted-storage-constructor)

For security the `Storage` constructor is distorted in Lightning Locker.

<!-- START generated embed: @locker/distortion/src/Storage/docs/constructor-value.md -->
## Storage API: Storage.prototype

The [`Storage`](https://developer.mozilla.org/en-US/docs/Web/API/Storage) interface provides access to a particular domain's session storage or local storage. It allows the addition, modification, or deletion of stored data items, which are shared.

The storage is accessible in the browser and holds its shape across multiple tabs from the same domain.

Lightning Web Security creates synthetic storage for each namespace, where malicious code can't add, modify, or clear data items in global storage or in storage belonging to other namespaces.

Note: The `key()` method of the `Storage` interface, when passed a number n, returns the name of the nth key in a given `Storage` object. The order of keys is defined by the user agent, so you can't rely on it. Therefore, it’s OK to have the storage items out of order.

### Distorted Behavior

This distortion prepends an `LSKey[NS]` to all storage values set in each namespace, where `NS` is the namespace name. This distortion uses a `SecureStorage` class that implements all methods and properties from the raw `Storage`. This distortion also uses a proxy to mimic interactive features that are on the raw `Storage`. Storage Example:

[Global]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y', 'LSKey[NS1]x': 'y', 'LSKey[NS2]x': 'y' }`

[NS1]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

[NS2]
`localStorage.setItem('x','y'); localStorage; // { 'x': 'y' }`

The proxy wrap has traps that allow for our Storage to have features that are the same as the raw Storage. Such features include getting, setting, iterating, and basic object features.

* Set/Get: `localStorage.x = 'y'; localStorage; // { 'x': 'y' }`
* Define Property: `Object.defineProperty(localStorage, 'foo', { value: 'bar' }); // { 'foo': 'bar', 'x': 'y' }`
* Delete Property: `delete localStorage.foo; // { 'x': 'y' }`
* Iteration: `Object.keys(localStorage); // ['x']`
* Has: `'x' in sessionStorage; localStorage.hasOwnProperty('x'); // true, true`
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/clear-value.md -->
## Storage.prototype.clear

The [`Storage.prototype.clear()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/clear) method clears all keys and associated data stored in a given `Storage` object.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `clear()` from clearing all the data items in another sandbox or outside sandboxes.

### Distorted Behavior

This distortion deletes all data items from the sandboxed code's synthetic storage.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/getItem-value.md -->
## Storage.prototype.getItem

The [`Storage.prototype.getItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/getItem) method, when passed a key name, returns that key's value, or `null` if the key does not exist, in the given `Storage` object.

Lightning Web Security creates synthetic storage for each sandbox. The synthetic storage prevents code in one sandbox from retrieving data belonging to another namespace or outside sandboxes.

### Distorted Behavior

This distortion ensures sandboxed code retrieves data items from its own synthetic storage.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/key-value.md -->
## Storage.prototype.key

The [`Storage.prototype.key()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/key) method, when passed a number n, returns the name of the nth key in a given `Storage` object. The order of keys is user-agent defined, so you can't rely on it. Therefore, it’s OK to have the storage items out of order.

### Distorted Behavior

This distortion retrieves a key value at a specific index from the sandboxed code's synthetic storage.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/length-getter.md -->
## Storage.prototype.length getter

The [`Storage.prototype.length`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/length) read-only property returns the number of data items stored in a given `Storage` object.

When the getter for `length` is used, Lightning Web Security retrieves the number of data items in the namespace's synthetic storage rather than the shared storage.

### Distorted Behavior

This distortion retrieves the number of data items in the sandboxed code's synthetic storage.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/removeItem-value.md -->
## Storage.prototype.removeItem

The [`Storage.prototype.removeItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/removeItem) method, when passed a key name, removes that key from the given `Storage` object if it exists.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `removeItem()` from removing data items from another sandbox or outside sandboxes.

### Distorted Behavior

This distortion deletes a data item from the sandboxed code's synthetic storage.
<!-- END generated embed, please keep comment -->

<!-- START generated embed: @locker/distortion/src/Storage/docs/setItem-value.md -->
## Storage.prototype.setItem

The [`Storage.prototype.setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem) method, when passed a key name and value,  adds that key to the given `Storage` object, or update that key's value if it already exists.

Each sandbox uses its own synthetic storage. Lightning Web Security prevents `setItem()`](https://developer.mozilla.org/en-US/docs/Web/API/Storage/setItem) from adding or modifying data items in another sandbox or outside sandboxes.
### Distorted Behavior

This distortion adds or modifies data items in the sandboxed code's synthetic storage.
<!-- END generated embed, please keep comment -->
