---
layout: home
title: "Wickra Proof — Proof-of-Backtest: a deterministic report plus a canonical blake3 hash from a (spec, data) pair, recomputable byte-for-byte in ten languages"
titleTemplate: false

hero:
  name: "Wickra Proof"
  text: "Proof-of-Backtest."
  tagline: "Turn a (spec, data) pair into a deterministic report and a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages."
  image:
    src: /wickra-mark.svg
    alt: "Wickra Proof"
  actions:
    - theme: brand
      text: View on GitHub
      link: https://github.com/wickra-lib/wickra-proof
    - theme: alt
      text: How it works
      link: /about

features:
  - icon: 🔒
    title: "A hash, not a screenshot"
    details: "The output is a canonical report and its blake3 digest. Two people with the same spec and the same data get the same 64 hex characters, or one of them is wrong."
  - icon: 🌍
    title: "Ten languages, one digest"
    details: "The report is canonicalised — sorted keys, quantised floats — before it is hashed, so the digest is identical whether it was produced from Rust, Python, Go or R."
  - icon: 📄
    title: "The spec is data"
    details: "A strategy is a JSON document, so what was proved is exactly what can be handed to someone else and run again."
  - icon: ⚙️
    title: "Built on the core"
    details: "The same deterministic engine and the same 514 indicators as the rest of the stack — the proof is over the arithmetic everything else already shares."
---
