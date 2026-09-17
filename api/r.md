# R

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for R. `install.packages("wickraproof", repos = "https://wickra-lib.r-universe.dev")` — over the C ABI via `.Call`, prebuilt library fetched on install.**

```r
install.packages("wickraproof", repos = "https://wickra-lib.r-universe.dev")
```

```r
library(wickraproof)

prover <- wkproof_new()
cmd <- paste0(
  '{"cmd":"prove","spec":{"strategy":{...},"dataset_ref":"BTCUSDT/1h"},',
  '"data":{"BTCUSDT":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}}'
)
cat(wkproof_command(prover, cmd), "\n")
# {"engine_version":"…","inputs_hash":"…","report":…,"report_hash":"…"}
cat(wkproof_version(), "\n")
```

## More

- [r-universe](https://wickra-lib.r-universe.dev)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/r)
