# Node

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for Node.js. `npm install wickra-proof` — prebuilt native binary, no system dependencies.**

```bash
npm install wickra-proof
```

```js
const { Prover } = require("wickra-proof");

const prover = new Prover();

const proof = JSON.parse(prover.command(JSON.stringify({
  cmd: "prove",
  spec: { strategy, dataset_ref: "BTCUSDT/1h" },
  data: { BTCUSDT: candles },
})));
console.log(proof.report_hash);

const verdict = JSON.parse(prover.command(JSON.stringify({
  cmd: "verify", proof, spec, data,
})));
// { ok: true, valid: true }
```

## More

- [npm](https://www.npmjs.com/package/wickra-proof)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/node)
