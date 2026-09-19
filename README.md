# [RUBÉN D. HIGUITA] | Systems & Telemetry Architect

> Low-Level & Deterministic Systems Engineer | Defense, Aerospace & Telemetry Domains.  
> Core Focus: POSIX-compliant daemons, non-blocking event-driven engines, zero-copy serialization, and real-time telemetry ingestion.

---

### System Architecture & Technical Specifications

| Domain | Implementations & Toolchains | Standards & Compliance |
| :--- | :--- | :--- |
| **Low-Level & Embedded** | C (C99/C11), Modern C++ (C++20), C++98, Rust | POSIX.1-2017, ISO/IEC 9899, MISRA-C |
| **Concurrency & Systems** | Multithreading, I/O Multiplexing (`epoll`), Lock-Free Buffers | Zero Dynamic Allocation in Fast-Path, Real-Time |
| **Telemetry & Networking**| Protocol Decoders, Bluetooth LE (`btleplug`), ZeroMQ, UDP Multicast | Tail-latency optimization, Bit-level Serialization |
| **Tooling & Verification**| Linux Kernel internals, GDB, Valgrind, LLVM Sanitizers (ASan/TSan) | IEEE 12207, MIL-STD-882E Architectural Models |

---

### Flagship Systems Architecture (Pinned Repositories)

#### 1. Non-Blocking Event-Driven Network Engine (C++98 / POSIX)
* **Target:** Servidor multiplexado sin dependencias externas sobre sockets no bloqueantes.
* **Architecture:** Máquina de Estados Finitos (FSM) determinista sobre `select`/`poll`/`epoll`.
* **Memory Model:** Cero asignaciones dinámicas (`heap`) dentro del bucle de eventos; reciclaje determinista de buffers.
* **Verification:** Perfil de memoria limpio verificado bajo Valgrind (0 bytes perdidos); compilación estricta bajo `-Wall -Wextra -Werror -pedantic`.

#### 2. High-Throughput Real-Time Telemetry Pipeline (Rust)
* **Target:** Ingestión y procesamiento de telemetría en tiempo real de flujo continuo sin latencia de asignación en tiempo de ejecución.
* **Architecture:** Demonio asíncrono de borde sobre BLE/Serial con canales lock-free SPSC (Single-Producer Single-Consumer).
* **Throughput:** Parser binario zero-copy con latencia de procesamiento tail en el rango de sub-microsegundos.
* **Safety:** Límites de `unsafe` formalmente delimitados y auditados vía `cargo clippy -- -D warnings` y `cargo miri`.

#### 3. Microservices & Network Virtualization Infrastructure (Docker / Nginx)
* **Target:** Infraestructura de red aislada y contenerizada, diseñada para despliegue determinista y tolerancia a fallos.
* **Architecture:** Segmentación estricta de servicios, terminación TLSv1.3 y demonios de inicialización POSIX sin overhead de systemd.

---

### Engineering Invariants

```text
+--------------------------------------------------------------------------+
| INVARIANT 1: Zero dynamic allocation (malloc/free/new) in critical paths |
| INVARIANT 2: Zero compiler warnings permitted (-Werror / Clippy deny)    |
| INVARIANT 3: Mandatory Sanitizer coverage (ASan, TSan, UBSan) in CI/CD   |
| INVARIANT 4: POSIX.1-2017 & ISO standard strict adherence                |
+--------------------------------------------------------------------------+
```
