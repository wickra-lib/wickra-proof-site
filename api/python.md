# Python

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for Python. `pip install wickra-proof` — prebuilt wheels for Linux, macOS and Windows, nothing to compile.**

```bash
pip install wickra-proof
```

```python
import json
from wickra_proof import Prover

prover = Prover()

proof = json.loads(prover.command(json.dumps({
    "cmd": "prove",
    "spec": {"strategy": strategy, "dataset_ref": "BTCUSDT/1h"},
    "data": {"BTCUSDT": candles},
})))
print(proof["report_hash"])

verdict = json.loads(prover.command(json.dumps({
    "cmd": "verify", "proof": proof, "spec": spec, "data": data,
})))
assert verdict == {"ok": True, "valid": True}
```

## More

- [PyPI](https://pypi.org/project/wickra-proof/)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/python)
