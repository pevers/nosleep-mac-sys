# nosleep-mac-sys

macOS library to block the power save function and preventing the OS to sleep.

## Usage

```toml
#Cargo.toml
[dependencies]
nosleep-mac-sys = "0.1.0"
```

## Documentation

The documentation can be found [here]().

## Example

```rust
use nosleep_mac_sys::*;
let handle = start(NoSleepType::PreventUserIdleSystemSleep);
if let Some(handle) = handle {
  println!("Block is active with handle {}", handle);
  stop(handle);
  println!("Block is deactivated");
}
```