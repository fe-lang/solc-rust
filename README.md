# solc-rust

Rust bindings for the [Solidity] compiler. It exposes [Compiler Input and Output JSON] API.

## Build
```
git clone --recursive git@github.com:Y-Nak/solc-rust.git
cargo build
```

## Usage

Add the dependency, as usual:

```toml
[dependencies]
solc = { git = "https://github.com/Y-Nak/solc-rust" }
```

In your project use it as:
```rust
pub fn main() {
    // Let input be a valid "Standard Solidity Input JSON"
    let input = "{}";
    let output = solc::compile(&input);
    assert_ne!(output.len(), 0);
}
```

## Maintainer(s)

Alex Beregszaszi

## License

GPL-3.0

[Solidity]: https://github.com/ethereum/solidity
[Compiler Input and Output JSON]: https://solidity.readthedocs.io/en/latest/using-the-compiler.html#compiler-input-and-output-json-description
