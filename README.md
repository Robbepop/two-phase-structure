# ink! - Two-phase compilation project structure

This show cases the project structure of ink! smart contracts post two-phase compilation process for ABI file generation.

## What has not changed

The smart contract source files remain in `src`.
The general smart contract `Cargo.toml` is still the one in root.
Note the additional `[workspace]` section there pointing into the hidden `.tools` folder.
There every tool, such as the initially planned `abi-gen` tool resides in its own directory.

For smart contracts not much change in regards to building and testing them.

## ABI generation: How-to

The metadata and ABI file generation is invoked as follows: `cargo run --package tools --bin abi_gen`

The `meta-gen` package in `.tools` is just there for demonstration purpose that multiple tools may co-exist later.