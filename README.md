# Rubén Darío Higuita Rubio

**Systems Engineer · Low-Level & Embedded Software**

---

#### Zero-Leak Architecture
Todo byte reservado se rastrea y libera de forma determinista.
Verificado con Valgrind y sanitizers en cada build.

#### Tactical Concurrency
Multihilo POSIX con prevención verificable de data races y deadlocks.

#### Minimalist Elegance
C/C++ depurado a su esencia. CI/CD que corre en cada push.

---

| Project | Architecture & Rigor | CI Pipeline |
|:---|:---|:---:|
| [`webserv`](https://github.com/higrub89/webserv) | HTTP/1.1 server · C++98 · `epoll` · zero leaks · 125% @ 42 | [![CI Verified](https://img.shields.io/badge/CI-VERIFIED-000000?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/higrub89/webserv/actions/workflows/ci.yml) |
| [`inception`](https://github.com/higrub89/inception) | Docker · NGINX · TLSv1.3 · isolated bridge network | [![CI Verified](https://img.shields.io/badge/CI-VERIFIED-000000?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/higrub89/inception/actions/workflows/ci.yml) |
| [`philosophers`](https://github.com/higrub89/philosophers) | Deadlock prevention · pthreads · TSan + Helgrind verified | [![CI Verified](https://img.shields.io/badge/CI-VERIFIED-000000?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/higrub89/philosophers/actions/workflows/ci.yml) |
| [`minishell`](https://github.com/higrub89/minishell) | POSIX shell · AST parser · fork/execve · signal-safe | [![CI Verified](https://img.shields.io/badge/CI-VERIFIED-000000?style=flat-square&logo=githubactions&logoColor=white)](https://github.com/higrub89/minishell/actions/workflows/ci.yml) |

---

```text
-Wall -Wextra -Werror -pedantic
Zero reachable bytes · Zero data races · CI-verified before merge
```

---

· [Sonovision Group](https://www.sonovisiongroup.com/) · Madrid · [42 Network](https://www.42network.org/) ·

[![LinkedIn](https://img.shields.io/badge/LinkedIn-000000?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/higrub89/)
[![Email](https://img.shields.io/badge/Email-000000?style=flat-square&logo=mail.ru&logoColor=white)](mailto:higuitaruben@hotmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=googlechrome&logoColor=white)](https://higrub89.github.io/)
[![42 Madrid](https://img.shields.io/badge/42_Madrid-000000?style=flat-square&logo=42&logoColor=white)](https://www.fundaciontelefonica.com/campus-42/)
