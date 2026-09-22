# Rubén D. Higuita
**Systems & Embedded Software Engineer | High-Performance Powertrain, Telemetry & Defense Systems**  
Madrid, Spain • [LinkedIn](https://www.linkedin.com/in/higrub89/) • `higuitaruben@hotmail.com` • [Portfolio](https://higrub89.github.io)

---

### Engineering Profile

Systems and embedded software engineer operating at the convergence of mission-critical hardware, deterministic real-time execution, and low-level software architecture. 

Over a decade of hands-on electromechanical and systems engineering across tier-one high-performance platforms (**Ferrari**, **Lamborghini**, **MV Agusta**) and high-voltage marine electro-propulsion (**SEABOB / CAYAGO AG**). Currently active inside the aerospace and defense engineering ecosystem (**Sonovision Ingenieros España**), authoring and validating systems-level technical documentation for tactical land vehicle platforms (Renault VPTL program), electrical schematic verification, and CAN-Bus network topologies.

This cross-disciplinary foundation unites hardware diagnostics, signal integrity, and fault isolation with deterministic memory management, concurrency arbitration, and POSIX-compliant systems programming.

---

### Systems Execution Hierarchy

```
+==========================================================================+
| APPLICATION & PROTOCOL LAYER                                             |
| Custom network daemons, telemetry parsers, multithreaded runtime engines |
+==========================================================================+
                              |
                              v  [Syscalls: socket, epoll, fork, pipe, mmap]
+==========================================================================+
| OS & RUNTIME ENVIRONMENT (POSIX.1-2017 / FreeRTOS)                       |
| Deterministic scheduling, virtual memory, pthreads, signal-safe traps   |
+==========================================================================+
                              |
                              v  [VFS, Register-Direct I/O, Hardware Buses]|
+==========================================================================+
| PHYSICAL & EMBEDDED INTERFACE LAYER                                      |
| STM32H7 (ARM Cortex-M7), CAN-FD (8 Mbps), ISO 11898, High-Voltage Powertrain|
+==========================================================================+
```

---

### Technical Capabilities & Standards

| Domain | Toolchain & Protocols | Standards & Verification |
| :--- | :--- | :--- |
| **Languages** | C (C99/C11), C++ (C++98/C++20), POSIX Shell, Assembly | ISO/IEC 9899, ISO/IEC 14882, MISRA C:2012 |
| **Embedded & Hardware** | STM32H743ZI (ARM Cortex-M7/M4), FreeRTOS, Bare-Metal | Register-direct peripheral access, zero-heap alloc |
| **Buses & Telemetry** | CAN 2.0A/B, CAN-FD (8 Mbps), SocketCAN, UART, SPI, I2C | ISO 11898-1:2015, RM0433 timing constraints |
| **Operating Systems** | Linux Kernel, POSIX.1-2017, Process Trees, IPC Pipelines | Deterministic IPC, `waitpid`, async-signal safety |
| **Networking & Daemons**| Non-blocking BSD sockets, I/O multiplexing (`epoll`, `poll`) | RFC 7230–7235 HTTP/1.1, FSM state machines |
| **Verification & Quality**| GCC, Clang, Makefiles, Valgrind Memcheck/Helgrind, TSan/ASan | `-Wall -Wextra -Werror -pedantic`, CI/CD |

---

### Flagship Systems & Architectures

#### 1. Hardware & Vehicle Telemetry
* **[`canfd-gateway-h7`](https://github.com/higrub89/canfd-gateway-h7)** — *High-Throughput CAN-FD Gateway Architecture for STM32H743ZI*  
  High-speed telemetry routing gateway operating at 8 Mbps data phase on ARM Cortex-M7. Implements direct-register peripheral configuration, zero-heap memory invariants, and FreeRTOS task segregation under MISRA C:2012 design constraints.

* **[`vehicle-can-telemetry-gateway`](https://github.com/higrub89/vehicle-can-telemetry-gateway)** — *Deterministic CAN Bus Telemetry Ingestion & Protocol Gateway*  
  Industrial telemetry ingestion pipeline in modern C++ utilizing Linux SocketCAN and lockless message ring buffers for sub-millisecond dispatch to upstream broker services.

#### 2. Network Daemons & Infrastructure
* **[`webserv`](https://github.com/higrub89/webserv)** — *POSIX.1-2017 Non-Blocking Event-Driven HTTP Engine*  
  Production-grade HTTP/1.1 web server in C++98. Asynchronous I/O multiplexing via single-threaded `epoll`/`poll` event loop, streaming FSM parser for chunked payloads, and isolated CGI process dispatch. Zero memory leaks validated with Valgrind (Pass with 125% bonus, 42 Madrid).

* **[`inception`](https://github.com/higrub89/inception)** — *High-Availability Microservices Infrastructure*  
  Enterprise containerized stack on pure Debian. TLSv1.3 cryptographic termination on custom NGINX, isolated WordPress (PHP-FPM) and MariaDB backends locked into an internal bridge network with zero host port leaks, enforced by an automated GitHub Actions security CI suite.

#### 3. Concurrency & POSIX Execution
* **[`philosophers`](https://github.com/higrub89/philosophers)** — *Hard Concurrency & Deadlock Prevention Harness*  
  Multithreaded shared-resource arbitration engine in C with POSIX mutex hierarchies. Microsecond-precision timing synchronization, verified clean of data races via ThreadSanitizer and Helgrind.

* **[`minishell`](https://github.com/higrub89/minishell)** — *POSIX-Compliant Command Execution Engine*  
  Unix execution runtime implementing an Abstract Syntax Tree (AST) parser, robust inter-process communication pipelines, file descriptor redirection, and async-signal-safe process lifecycle control.

---

### Professional Background & Credentials

* **Systems Software Engineering** — *42 Madrid (Fundación Telefónica)*. Common Core advanced systems curriculum.
* **Technical Authoring & Systems Engineering** — *Sonovision Ingenieros España* (Aerospace & Defense). Technical repair, maintenance, and systems architecture documentation for the tactical Renault VPTL military vehicle program; electrical schematic interpretation and CAN-Bus topology validation.
* **Certified High-Performance Electro-Drive Specialist** — *CAYAGO AG (Bad Salzuflen, Germany)*. Certified diagnostics and powertrain service on SEABOB F5 and F9 high-voltage marine electro-propulsion systems.
* **Precision Automotive Engineering Experience** — Hands-on diagnostic, powertrain, and electromechanical engineering across supercar and high-performance racing platforms (**Ferrari**, **Lamborghini**, **MV Agusta**).
* **Cross-Platform Software Engineering (DAM)** — *CIPFPD La Rioja* (In progress, bridging to B.Sc. in Computer Engineering).

---

### Non-Negotiable Engineering Invariants

```text
1. Memory Hygiene      : Zero reachable bytes / zero leaks under Valgrind Memcheck and ASan.
2. Thread Safety       : Zero data races verified deterministically via TSan and Helgrind.
3. Toolchain Rigor     : Strict compilation with -Wall -Wextra -Werror -pedantic.
4. Defense Compliance  : Modular segregation of concerns (SoC), defensive boundary validation, zero secret commits.
```
