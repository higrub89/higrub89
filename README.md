# Rubén D. Higuita

## Systems Engineer · Low-Level & Embedded Software

Madrid, Spain

[LinkedIn](https://www.linkedin.com/in/higrub89/) · [Portfolio](https://higrub89.github.io) · `higuitaruben@hotmail.com`

---

### Background

Ingeniería que combina una década de experiencia electromecánica de alto
rendimiento con desarrollo de software de bajo nivel en C/C++ y POSIX.

Formado en el diagnóstico de fallos mecánicos bajo tolerancias extremas,
aplico la misma disciplina al software: gestión de memoria determinista,
cero condiciones de carrera, código auditable de principio a fin.

#### Zero-Leak Architecture
Todo byte reservado y todo socket abierto se rastrea y libera de forma
determinista, verificado con Valgrind y sanitizers en cada build.

#### Tactical Concurrency
Programación multihilo y sincronización POSIX, con prevención verificable
de data races y deadlocks.

#### Minimalist Elegance
Código C/C++ depurado a su esencia: modular, con separación de
responsabilidades y CI/CD que corre en cada push, no solo en la
descripción.

---

### Industry Experience

**Defense & Aerospace — ILS Engineering**
Sonovision Ingenieros España. Integrated Logistics Support (ILS) for tactical military vehicle programs. Authoring and validation of technical repair and maintenance documentation for armored and utility platforms: **VEMPAR**, **VPTL** (Renault Trucks Defense), and **multilift tipper platforms**. Electrical schematic interpretation, wiring harness verification, and CAN-Bus network topology analysis for documentation accuracy across defense-grade ground systems.

**Hyperluxury Automotive — Supercars**
Ferrari, Lamborghini. Complete powertrain diagnostics, electronic fault isolation, and high-voltage systems servicing on V8/V10/V12 naturally aspirated and turbocharged architectures. OBD-II / proprietary diagnostic protocol interfacing.

**High-Performance Motorcycles**
MV Agusta, Ducati, Honda, Yamaha. Engine management calibration, fuel injection mapping, suspension geometry setup, and race-preparation mechanical builds across inline-4, V-twin, and L-twin configurations.

**Marine & Aquatic Propulsion**
SEABOB (CAYAGO AG, Germany) — Certified specialist in high-voltage electric-drive diagnostics and powertrain service for F5 and F9 marine propulsion units. Jet Ski Kawasaki — 2-stroke and 4-stroke marine engine overhaul and watercraft hull systems.

**Off-Road & Utility Vehicles**
CF Moto buggies and quads. Powertrain service, CVT transmission systems, and electrical diagnostics across utility and recreational all-terrain platforms.

---

### Software Engineering

Currently building deep systems-level foundations through two concurrent academic tracks and professional-grade project work:

**42 Madrid** (Fundación Telefónica) — Peer-reviewed systems software engineering curriculum. Common Core in progress. All projects compiled under strict `-Wall -Wextra -Werror`, verified with Valgrind Memcheck and ThreadSanitizer, and deployed with GitHub Actions CI pipelines.

**DAM — Desarrollo de Aplicaciones Multiplataforma** (CIPFPD La Rioja, distance) — Cross-platform application development. Object-oriented design, software architecture patterns, and database systems.

**Additional Certifications:**
- Advanced Linux Professional Administration (IFCT066PO, 100h) — SEPE / Comunidad de Madrid
- .NET & C# Object-Oriented Programming
- Software Engineering Methodologies for the Web

---

### Technical Stack

| Layer | Technologies | Standards |
| :--- | :--- | :--- |
| **Languages** | C (C99/C11), C++ (C++98/C++20), POSIX Shell | ISO 9899, ISO 14882, MISRA C:2012 |
| **Embedded** | STM32H743ZI (ARM Cortex-M7), FreeRTOS, Bare-Metal | Register-direct I/O, zero-heap invariants |
| **Buses** | CAN 2.0A/B, CAN-FD (8 Mbps), SocketCAN, UART, SPI | ISO 11898-1:2015 |
| **Systems** | Linux Kernel, POSIX.1-2017, IPC Pipelines, Pthreads | Deterministic process lifecycle |
| **Networking** | Non-blocking BSD sockets, `epoll`/`poll` multiplexing | RFC 7230–7235 HTTP/1.1, FSM parsers |
| **Verification** | Valgrind, Helgrind, TSan, ASan, GDB, Clang, GCC | `-Wall -Wextra -Werror -pedantic` |
| **Infrastructure** | Docker, NGINX, TLSv1.3, GitHub Actions CI/CD | Network isolation, secret audit |

---

### Selected Projects

**Embedded & Vehicle Telemetry**

[`canfd-gateway-h7`](https://github.com/higrub89/canfd-gateway-h7) — CAN-FD gateway on STM32H743ZI. 8 Mbps data phase, register-direct peripheral configuration, FreeRTOS task segregation, MISRA C:2012 compliance.

[`vehicle-can-telemetry-gateway`](https://github.com/higrub89/vehicle-can-telemetry-gateway) — Industrial telemetry ingestion pipeline. Linux SocketCAN, lockless ring buffers, sub-millisecond broker dispatch.

**Network Services & Infrastructure**

[`webserv`](https://github.com/higrub89/webserv) — HTTP/1.1 server in C++98. Single-threaded `epoll` event loop, FSM chunked parser, CGI subprocess isolation. Zero memory leaks. Pass with 125% bonus (42 Madrid).

[`inception`](https://github.com/higrub89/inception) — Containerized microservices stack. NGINX with TLSv1.3 termination, WordPress and MariaDB on isolated bridge network. Automated security CI suite.

**Concurrency & POSIX Runtime**

[`philosophers`](https://github.com/higrub89/philosophers) — Multithreaded deadlock prevention engine. POSIX mutex hierarchies, microsecond-precision timing. Zero data races (TSan + Helgrind verified).

[`minishell`](https://github.com/higrub89/minishell) — POSIX command execution runtime. AST parser, `fork`/`execve`/`waitpid` process trees, `dup2` stream redirection, async-signal-safe traps.

**Algorithmic & Systems Primitives**

[`push_swap`](https://github.com/higrub89/push_swap) — Constrained stack sorting engine. K-Sort partitioning with O(n√n) operational complexity.

[`cub3d`](https://github.com/higrub89/cub3d) — Real-time software raycasting engine. DDA grid traversal, direct framebuffer writes, zero GPU dependencies.

[`pipex`](https://github.com/higrub89/pipex) — UNIX IPC pipeline implementation. Kernel pipe buffers, atomic `dup2` redirection, deterministic FD lifecycle.

---

### Engineering Constraints

```
Memory         Zero reachable bytes under Valgrind Memcheck and ASan
Concurrency    Zero data races under TSan and Helgrind
Compilation    -Wall -Wextra -Werror -pedantic on every build
Commits        Conventional Commits, atomic scope, CI-verified before merge
```

---

```
LOCATION: MADRID · 42 NETWORK · SONOVISION INGENIEROS
```
