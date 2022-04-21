# nosleep-mac-sys

[![Continuous Integration](https://github.com/pevers/nosleep-mac-sys/actions/workflows/ci.yml/badge.svg)](https://github.com/pevers/nosleep-mac-sys/actions/workflows/ci.yml)
![Crates.io](https://img.shields.io/badge/platform-macOS-lightgrey?style=flat-square)
[![license](https://img.shields.io/crates/l/nosleep-mac-sys?style=flat-square)](https://crates.io/crates/nosleep-mac-sys/)
[![version](https://img.shields.io/crates/v/nosleep-mac-sys?style=flat-square)](https://crates.io/crates/nosleep-mac-sys/)
![Crates.io](https://img.shields.io/crates/d/nosleep-mac-sys?style=flat-square)

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