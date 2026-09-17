# Java

**Proof-of-Backtest. Turn a `(spec, data)` pair into a deterministic backtest report *and* a canonical blake3 hash that anyone can recompute byte-for-byte in ten languages — for Java. `org.wickra:wickra-proof` — prebuilt native library inside the jar, no JNI, no system dependencies.**

```xml
<dependency>
  <groupId>org.wickra</groupId>
  <artifactId>wickra-proof</artifactId>
  <version>0.1.2</version>
</dependency>
```

```java
import org.wickra.proof.Prover;

try (Prover prover = new Prover()) {
    String cmd = """
        {"cmd":"prove","spec":{"strategy":{...},"dataset_ref":"BTCUSDT/1h"},
        "data":{"BTCUSDT":[{"time":1,"open":100,"high":101,"low":99,"close":100,"volume":1000}]}}""";
    System.out.println(prover.command(cmd));
    // {"engine_version":"…","inputs_hash":"…","report":…,"report_hash":"…"}
}
System.out.println(Prover.version());
```

## More

- [Maven Central](https://central.sonatype.com/artifact/org.wickra/wickra-proof)
- [Source & examples](https://github.com/wickra-lib/wickra-proof/tree/main/examples/java)
