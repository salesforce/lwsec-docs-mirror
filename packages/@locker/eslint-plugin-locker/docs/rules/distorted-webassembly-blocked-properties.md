# Distorted WebAssembly blocked properties (distorted-webassembly-blocked-properties)

For security WebAssembly properties are blocked by Lightning Web Security.

## Rule Details

This rule warns when code tries to access blocked WebAssembly properties that could potentially be used for sandbox escapes.

### Blocked Properties

The following WebAssembly properties are blocked:

- `WebAssembly.compile` - Compiles a WebAssembly module from binary data
- `WebAssembly.compileStreaming` - Compiles a WebAssembly module from a streaming source
- `WebAssembly.instantiate` - Instantiates a WebAssembly module
- `WebAssembly.instantiateStreaming` - Instantiates a WebAssembly module from a streaming source
- `WebAssembly.validate` - Validates a WebAssembly binary
- `WebAssembly.Module` - Constructor for WebAssembly modules
- `WebAssembly.Instance` - Constructor for WebAssembly instances
- `WebAssembly.Memory` - Constructor for WebAssembly memory
- `WebAssembly.Table` - Constructor for WebAssembly tables
- `WebAssembly.Global` - Constructor for WebAssembly globals
- `WebAssembly.Tag` - Constructor for WebAssembly tags
- `WebAssembly.CompileError` - WebAssembly compile error constructor
- `WebAssembly.LinkError` - WebAssembly link error constructor
- `WebAssembly.RuntimeError` - WebAssembly runtime error constructor
- `WebAssembly.Exception` - WebAssembly exception constructor

## Examples

###  Incorrect

```js
// Trying to compile WebAssembly
const module = WebAssembly.compile(wasmBinary);

// Trying to instantiate WebAssembly
WebAssembly.instantiate(wasmBinary);

// Trying to create WebAssembly objects
const x = new WebAssembly.Module(wasmBinary);
const y = new WebAssembly.Instance(module);
```