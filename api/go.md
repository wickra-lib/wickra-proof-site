# Go

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for Go. `go get github.com/wickra-lib/wickra-proof-go` — over the C ABI via cgo, prebuilt library bundled in the module.**

```bash
go get github.com/wickra-lib/wickra-proof-go
```

```go
package main

import (
	"fmt"

	wickra "github.com/wickra-lib/wickra-proof-go"
)

func main() {
	p := wickra.New()
	defer p.Close()

	cmd := `{"cmd":"prove","spec":{"strategy":{...},"dataset_ref":"BTCUSDT/1h"},` +
		`"data":{"BTCUSDT":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}}`

	proof, err := p.Command(cmd)
	if err != nil {
		panic(err)
	}
	fmt.Println(proof) // {"engine_version":"…","inputs_hash":"…","report":…,"report_hash":"…"}
	fmt.Println(wickra.Version())
}
```

## More

- [pkg.go.dev](https://pkg.go.dev/github.com/wickra-lib/wickra-proof-go)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/go)
