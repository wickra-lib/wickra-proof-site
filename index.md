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

<script setup>
const installTabs = [
  { label: 'Python', lang: 'bash', code: 'pip install wickra-proof' },
  { label: 'Node', lang: 'bash', code: 'npm install wickra-proof' },
  { label: 'Rust', lang: 'bash', code: 'cargo add wickra-proof-core' },
  { label: 'WASM', lang: 'bash', code: 'npm install wickra-proof-wasm' },
  { label: 'C', lang: 'bash', code: '# prebuilt header + library from GitHub releases:\n# github.com/wickra-lib/wickra-proof/releases' },
  { label: 'C#', lang: 'bash', code: 'dotnet add package Wickra.Proof' },
  { label: 'Go', lang: 'bash', code: 'go get github.com/wickra-lib/wickra-proof-go' },
  { label: 'Java', lang: 'xml', code: '<!-- Maven Central -->\n<dependency>\n  <groupId>org.wickra</groupId>\n  <artifactId>wickra-proof</artifactId>\n  <version>0.1.3</version>\n</dependency>' },
  { label: 'R', lang: 'r', code: 'install.packages("wickraproof", repos = "https://wickra-lib.r-universe.dev")' },
]
</script>

## Install

The same engine from every language — native Rust, Python, Node.js and WASM, plus a C
ABI for C, C++, C#, Go, Java and R.

<InstallTabs :tabs="installTabs" />

The [API pages](/api/rust) carry a quick start per language; the
[repository README](https://github.com/wickra-lib/wickra-proof#readme) the same in one place.

## Built on the Wickra core

Wickra Proof is part of the [Wickra](https://wickra.org) ecosystem — one indicator core,
twenty-three products, the same ten-language binding surface in every one of them,
checked byte-for-byte by a golden corpus in every repository.

> Wickra Proof is a software library, not a trading system, and gives no financial
> advice — its outputs are deterministic transforms of the input data and do not
> predict future returns. Use it at your own risk.
