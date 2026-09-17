# Rust

The native crate — the same engine every other binding of Wickra Proof wraps.

```bash
cargo add wickra-proof-core
```

```rust
use wickra_proof_core::{prove, verify, ProofSpec};

// A ProofSpec is the strategy and a dataset reference; the candles are
// supplied beside it. `prove` folds the two into a report and its hashes.
let spec = ProofSpec::from_json(spec_json)?;
let proof = prove(&spec, &candles_by_symbol)?;
println!("report_hash: {}", proof.report_hash);

// Anyone with the same spec and data recomputes the same bytes, in any of
// the ten languages -- and a proof that does not recompute is not valid.
assert!(verify(&proof, &spec, &candles_by_symbol)?);
```

## More

- [crates.io/crates/wickra-proof-core](https://crates.io/crates/wickra-proof-core)
- [docs.rs](https://docs.rs/wickra-proof-core)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples)
