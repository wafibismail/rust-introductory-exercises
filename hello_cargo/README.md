# Hello, Cargo

Cargo is Rust's build system and package manager. It:
- Builds code
- Downloads libraries the code depends on
  - and building those libraries.

## Create, build, check and run a project

```ps
cargo new hello_cargo
cd hello_cargo
```

Creates:
- Cargo.toml
- src\main.rs

Cargo.toml:

```Rust
[package]
name = "hello_cargo"
version = "0.1.0"
edition = "2021"

[dependencies]
```

Inside auto-generated src\main.rs

```Rust
fn main() {
    println!("Hello, world!");
}
```

Build the project, which creates the .exe files, etc in a target folder:

```ps
cargo build
```

Run the project:

```ps
cargo run
```

Build for release (slower than regular build):

```ps
cargo build --release
```

Check for compilation errors (faster than having to build):

```ps
cargo check
```