# Rubén D. Higuita
**Low-Level Systems Developer | C / C++ / POSIX — building toward Defense & Aerospace Software Engineering**
Madrid, Spain • [LinkedIn](https://www.linkedin.com/in/higrub89/) • [GitHub](https://github.com/higrub89)

---

### Engineering Profile

Transitioning from a decade of hands-on mechanical and electromechanical engineering — automotive, high-performance marine propulsion, industrial assembly — into systems-level software development. Currently building deep C/C++/POSIX foundations through 42 Madrid's peer-reviewed curriculum while working professionally inside Spain's defense-industry technical documentation chain.

The combination is deliberate: fault isolation, electrical schematic interpretation, and hardware diagnostics from the mechanical side; deterministic memory management and POSIX systems programming from the software side.

---

### Systems Execution Model

```
+--------------------------------------------------------------------------+
| APPLICATION & DAEMON LAYER                                               |
| Custom network daemons, FSM protocol parsers, multithreaded engines      |
+--------------------------------------------------------------------------+
                              |
                              v  [Syscalls: socket, poll/epoll, fork, pipe]
+--------------------------------------------------------------------------+
| OS & POSIX RUNTIME ENVIRONMENT (POSIX.1-2017)                            |
| Process lifecycles (waitpid), signal safety, virtual memory, pthreads    |
+--------------------------------------------------------------------------+
                              |
                              v  [VFS, Kernel Buffers, Hardware Buses]
+--------------------------------------------------------------------------+
| PHYSICAL & HARDWARE INTERFACE LAYER                                      |
| Electronic diagnostics, bus communications, high-power electro-drive     |
+--------------------------------------------------------------------------+
```

---

### Technical Capabilities

| Domain | Toolchain & Specifications | Standards |
| :--- | :--- | :--- |
| **Languages** | C (C99/C11), C++ (C++98/C++20), POSIX Shell scripting | ISO/IEC 9899, ISO/IEC 14882 |
| **OS & Kernel** | Linux kernel configuration, syscalls, process trees, IPC (pipes, FIFOs) | POSIX.1-2017 |
| **Concurrency & IPC** | POSIX Threads (`pthreads`), mutexes, async-signal-safe handling | Data-race free, deterministic sync |
| **Networking & I/O** | Non-blocking BSD sockets, I/O multiplexing (`epoll`, `poll`, `select`) | State-machine driven |
| **Verification** | GCC, Clang, Makefiles, GDB, Valgrind, Sanitizers (ASan, TSan) | `-Wall -Wextra -Werror -pedantic` |
| **Hardware & Electronics** | Electronic diagnostics, bus signals, high-voltage powertrain systems | Industrial field tolerances, schematic analysis |

---

### Featured Projects (42 Madrid)

#### `webserv` — Non-Blocking HTTP/1.1 Server
Event-driven network service in C++98, no external runtime libraries. Single-threaded polling architecture (`poll`/`epoll`) for asynchronous client streams, with a finite-state-machine parser for chunked HTTP requests and isolated CGI subprocess dispatch.
**Result:** Pass with bonus (42 Madrid, 18/09/2026).
[github.com/higrub89/webserv](https://github.com/higrub89/webserv)

#### `minishell` — POSIX Shell Implementation
Unix command execution runtime in C: process trees (`fork`, `execve`), file descriptor redirection (`dup2`), deterministic process lifecycle via `waitpid`, and POSIX-async-signal-safe signal trapping (`SIGINT`, `SIGQUIT`).
[github.com/higrub89/minishell](https://github.com/higrub89/minishell)

#### `philosophers` — Concurrent Resource Synchronization
Multithreaded simulation resolving shared-resource contention under microsecond-level timing constraints, with mutex arbitration to eliminate deadlocks and starvation.
[github.com/higrub89/philosophers](https://github.com/higrub89/philosophers)

#### `cub3d` — Fixed-Point Raycasting Engine
Real-time software renderer in C, writing directly to raw framebuffers, using DDA grid traversal to minimize floating-point operations.
[github.com/higrub89/cub3d](https://github.com/higrub89/cub3d)

---

### Background & Certifications

* **42 Madrid (Fundación Telefónica)** — Systems Software Engineering curriculum. Common Core: 87% validated (in progress).
* **Formación Profesional — Desarrollo de Aplicaciones Multiplataforma (DAM)**, CIPFPD La Rioja — in progress, bridging toward a Bachelor's in Computer Engineering.
* **Technical Authoring & Systems Documentation** — Sonovision Ingenieros España (Defense & Aerospace engineering services provider). Authoring and validation of technical repair/maintenance manuals for the VPTL Renault program, including interpretation of electrical schematics and CAN-Bus networks for documentation accuracy.
* **High-Performance Electro-Propulsion Certification** — CAYAGO AG (Bad Salzuflen, Germany). Certified diagnostics and service on SEABOB F5 and F9 high-voltage electric-drive systems.
* **Advanced Linux Professional Certification (IFCT066PO, 100h)** — SEPE / Comunidad de Madrid. *(confirm exact issuing training center before publishing)*

---

### Engineering Constraints I Hold Myself To

```text
1. Toolchain compliance    : gcc/g++ -Wall -Wextra -Werror -pedantic
2. Memory policy           : zero reachable/leaked bytes in persistent services
3. Concurrency invariants  : zero data races (TSan-verified), deterministic lock ordering
```
