# WASM

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for WASM. `npm install wickra-proof-wasm` — pure WebAssembly, runs anywhere a modern JS engine does.**

```bash
npm install wickra-proof-wasm
```

```js
import init, { Prover, version } from "wickra-proof-wasm";

await init();

const prover = new Prover();
const proof = JSON.parse(
  prover.command(JSON.stringify({ cmd: "prove", spec, data })),
);
// proof.report_hash / proof.inputs_hash are 64-hex blake3 digests, identical
// to the native CLI for the same (spec, data).

const verdict = JSON.parse(
  prover.command(JSON.stringify({ cmd: "verify", proof, spec, data })),
);
// { ok: true, valid: true }

console.log(version()); // the library version
```

## More

- [npm](https://www.npmjs.com/package/wickra-proof-wasm)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/wasm)
