# C#

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for C#. `dotnet add package Wickra.Proof` — prebuilt native library, no system dependencies.**

```bash
dotnet add package Wickra.Proof
```

The binding is a thin, faithful surface over the same command boundary every other binding drives, so a request built here produces the same canonical bytes it would in Rust, Python or Go.

```csharp
using WickraProof;

using var handle = new Prover();
string response = handle.Command("""{"cmd":"version"}""");
Console.WriteLine(response);
```

## More

- [NuGet](https://www.nuget.org/packages/Wickra.Proof)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/csharp)
