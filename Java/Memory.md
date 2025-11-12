# Java Memory — Why learn it & core structure

## Why learning Java memory matters
- Java is a language with automatic memory management: the JVM handles allocation and deallocation to reduce manual errors (e.g., dangling pointers).
- Despite automatic GC, memory issues (leaks, shortages, OOM) still occur and often require human diagnosis and tuning.
- Understanding memory layout helps you tune performance, diagnose leaks, and prevent outages.

## High-level split
- Heap: where application objects live (subject to GC).
- Metaspace (replaced PermGen since Java 8): stores class metadata, static info.
- Stack: per-thread call frames and local variables.
- Native / code cache: JVM internals and JIT-compiled code.

---

## Metaspace
- Stores class metadata, method info, classloaders, interned strings (depending on Java version).
- Unlike PermGen, Metaspace grows dynamically up to available system memory unless bounded.
- Common tuning flags:
  - -XX:MetaspaceSize — initial threshold for Metaspace GC.
  - -XX:MaxMetaspaceSize — upper limit for Metaspace.
  - -XX:MinMetaspaceFreeRatio / -XX:MaxMetaspaceFreeRatio — control free space after GC.

---

## Heap (overview)
- Heap holds objects allocated with new and is managed by the GC.
- Divided into:
  - Young Generation (Eden + two Survivor spaces S0/S1)
  - Old (Tenured) Generation — long-lived objects
- Large/humongous objects may be allocated directly into Old Gen depending on JVM and GC.

### Young Gen
- Eden: first allocation area (often uses TLAB per thread).
- Survivor spaces (S0/S1 / From/To): temporary holders for objects surviving a minor GC.
- Minor GC: triggered when Eden fills — live objects are copied to a survivor, ages incremented.

### Survivor behavior & promotion
- Survivor spaces implement a copying algorithm: live objects are copied between S0 and S1 on successive minors.
- Objects surviving enough cycles (age >= tenuring threshold) or when survivor space is low are promoted to Old Gen.
- Tenuring threshold can be tuned (e.g., -XX:MaxTenuringThreshold) or adaptive.

### Old Generation
- Stores long-lived objects promoted from Young Gen.
- Collected less frequently; collection strategies vary (mark-sweep-compact, concurrent collectors).
- Full/major GC is more expensive and can cause noticeable pauses.

---

## Common GC and tuning knobs (concise)
- Heap sizing: -Xms (initial), -Xmx (max)
- Young size: -Xmn or set via -XX:NewRatio
- Survivor sizing: -XX:SurvivorRatio
- Tenuring: -XX:MaxTenuringThreshold, -XX:+UseAdaptiveSizePolicy
- Collector choice: -XX:+UseG1GC, -XX:+UseParallelGC, -XX:+UseConcMarkSweepGC, etc.
- Metaspace: -XX:MetaspaceSize, -XX:MaxMetaspaceSize
- Additional: -XX:+HeapDumpOnOutOfMemoryError, -Xloggc:<file> (or modern -Xlog options), -XX:ParallelGCThreads
- New-size flags mentioned: -XX:NewSize / -XX:MaxNewSize (Eden sizing in some JVMs)

---

## Why monitor Java memory
- Detect memory leaks before they cause OOM.
- Optimize GC and heap settings to reduce pause times and throughput impact.
- Prevent OutOfMemoryError by ensuring adequate sizing.
- Troubleshoot issues like excessive GC, memory thrashing, or inefficient allocation patterns.

How to monitor:
- Built-in tools: jstat, jmap, jcmd, Java VisualVM, Java Mission Control.
- Heap dump analysis: Eclipse MAT, VisualVM to inspect retained set and leak suspects.
- Production monitoring: Prometheus + exporters, Grafana, New Relic, Datadog.
- Logging & alerts: GC logs, memory thresholds and automated alerts.

---

## Quick summary
- Java automates memory management, but developers must still understand memory regions (Eden, Survivor, Old, Metaspace) to tune, diagnose, and fix issues.
- Objects flow: Eden → Survivor(s) → Old (based on age/space). GC types: Minor (young) vs Major/Full (old).
- Proper sizing, GC selection, and monitoring are essential for stable, performant Java apps.
