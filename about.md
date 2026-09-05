# About Wickra Proof

Turn a (spec, data) pair into a deterministic report and a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages.

## What it does

Wickra Proof takes a strategy specification and a dataset, recomputes the backtest deterministically, and emits the report together with the blake3 hash of its canonical form. The hash is the artefact: it is short enough to publish and exact enough that recomputing it is a real check.

## Why it exists

A backtest screenshot proves nothing. A number anyone can independently recompute from the same two inputs is a claim that can be checked rather than believed.

## Open source

Released under the **MIT OR Apache-2.0** license — permissive, OSI-approved and
free for any use, including commercial. Source, issues and releases on
[GitHub](https://github.com/wickra-lib/wickra-proof).

## Disclaimer

Wickra Proof is software, **not** a trading system, and is provided **as-is with no
warranty**. It does not give financial advice. Use it at your own risk.
