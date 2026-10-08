# 42 Tokyo — Common Core Projects

A portfolio of my projects from the **42 Tokyo Common Core**, documenting my progress in systems programming, algorithms, Linux administration, and Python development.

I joined 42 Tokyo in **April 2026** after completing the Piscine. This repository is a **project index**: source code is maintained in separate repositories, while this page highlights the problems solved, implementation choices, and skills developed.

## Projects at a Glance

| Project | Language / Tools | Focus | Source |
| --- | --- | --- | --- |
| **Libft** | C, Makefile | C utilities, pointers, memory, linked lists | [Repository](https://github.com/Ranran-bagel/42_libft) |
| **ft_printf** | C, Makefile | Variadic arguments, formatted output | [Repository](https://github.com/Ranran-bagel/42_ft_printf) |
| **get_next_line** | C | Buffered file I/O, static storage, multiple file descriptors | [Repository](https://github.com/Ranran-bagel/42_get_next_line) |
| **Born2beroot** | Debian, Linux, SSH, UFW | VM setup, access control, system security | [Details](#born2beroot) |
| **push_swap** | C, Makefile | Sorting algorithms, complexity, benchmarking | [Repository](https://github.com/Ranran-bagel/42_push_swap) |
| **A-Maze-ing** | Python, MiniLibX | Maze generation, pathfinding, reusable packages | [Repository](https://github.com/Ranran-bagel/42_a_maze_ing) |
| **Python Modules** | Python, mypy, Poetry, Pydantic | OOP, typing, decorators, packaging, validation | [Repository](https://github.com/Ranran-bagel/42_python_modules) |

## Project Highlights

### Libft

**Building a reusable C library from scratch.**

Reimplemented common C library functionality and created additional utilities, compiled into the static library `libft.a`. The work covers character and string operations, memory manipulation, dynamic allocation, file-descriptor output, and linked-list utilities.

**What I practiced:** pointer arithmetic, allocation and cleanup, linked-list operations, modular function design, and building a static library with Make.

**Source:** [42_libft](https://github.com/Ranran-bagel/42_libft)

### ft_printf

**Implementing formatted output with variadic functions.**

Built a custom `ft_printf` that parses a format string, retrieves arguments using `va_list`, and writes the formatted result to standard output. Supports `%c`, `%s`, `%p`, `%d`, `%i`, `%u`, `%x`, `%X`, and `%%`, returning the number of characters printed. The implementation focuses on the mandatory conversions rather than bonus formatting flags.

**What I practiced:** variadic arguments, type-specific conversion, hexadecimal formatting, output accounting, and decomposition into helper functions.

**Source:** [42_ft_printf](https://github.com/Ranran-bagel/42_ft_printf)

### get_next_line

**Reading text incrementally from file descriptors.**

Implemented `get_next_line(int fd)` to return one line per call using `read()` and a configurable `BUFFER_SIZE`. The function preserves unread content between calls and handles newline boundaries and end-of-file conditions. The repository also includes bonus files for handling multiple file descriptors.

**What I practiced:** buffered I/O, static variables, dynamic memory management, error handling, and maintaining state across function calls.

**Source:** [42_get_next_line](https://github.com/Ranran-bagel/42_get_next_line)

### Born2beroot

**Configuring and securing a Linux virtual machine.**

Set up a Debian-based virtual machine and worked with the system administration and security requirements of the Born2beroot project, including:

- User and group administration, privilege management, and `sudo` configuration.
- SSH configuration, including disabling direct root SSH login.
- UFW firewall rules and password-policy configuration.
- Storage and partitioning concepts, including LVM.
- System monitoring and basic resource reporting.

**What I practiced:** Linux administration, authentication and authorization, network access, firewall configuration, and explaining system settings during peer evaluation.

*This project is documented here because its main deliverable is a configured virtual machine rather than a conventional source-code repository. VM images, credentials, and private configuration are not published.*

### push_swap

**Sorting integers using two stacks and a restricted instruction set.**

Developed a sorting program that emits operations such as `sa`, `pb`, `ra`, and `rrr` to sort a stack with as few instructions as practical. The project includes several strategies:

- **Small-input routines:** dedicated handling for up to five elements.
- **Simple:** insertion-style sorting, **O(n²)**.
- **Medium:** chunk-based sorting, **O(n√n)**.
- **Complex:** binary radix sorting, **O(n log n)**.
- **Adaptive:** selects a strategy based on a disorder metric.

The repository also contains a bonus **checker** that reads operations from standard input and verifies the result, plus a benchmark mode reporting strategy selection and operation counts. In this collaborative project, I contributed to the medium sorting strategy, small-input handling, checker, stack operations, and error handling; my teammate contributed to other parts of the implementation.

**What I practiced:** algorithm selection, complexity analysis, stack operations, input validation, testing, benchmarking, and collaborative development.

**Source:** [42_push_swap](https://github.com/Ranran-bagel/42_push_swap)

### A-Maze-ing

**Generating, analyzing, and visualizing mazes in Python.**

Built a configuration-driven maze generator with a teammate. The application supports perfect and non-perfect mazes, reproducible generation with seeds, shortest-path computation, hexadecimal wall encoding, and an interactive MiniLibX visualization. It also incorporates a visible **“42”** pattern into the maze layout.

The maze-generation logic is separated into a reusable **`mazegen` Python package**, independent of the application entry point and renderer. The project includes configuration validation, build/run commands, and lint/type-check workflows.

**What I practiced:** graph traversal, depth-first search, breadth-first search, modular architecture, Python packaging, graphical rendering, and collaborative debugging.

**Source:** [42_a_maze_ing](https://github.com/Ranran-bagel/42_a_maze_ing)

### Python Modules

**Learning Python through progressively more advanced exercises.**

A collection of Python exercises organized by module, moving from language fundamentals toward maintainable, typed, and configurable programs. Topics covered across the modules include:

- Python syntax, collections, functions, file I/O, and command-line arguments.
- Exceptions and object-oriented programming.
- Iterators, generators, and decorators.
- Type hints and strict static checking with **mypy**.
- Generic typing with **`TypeVar`** and **`ParamSpec`**.
- Virtual environments and dependency management with **pip** and **Poetry**.
- Environment variables and `.env` configuration.
- Data models and validation with **Pydantic**, including nested models and custom validators.

**What I practiced:** writing maintainable Python, API design, type safety, package management, and validation of structured data.

**Source:** [42_python_modules](https://github.com/Ranran-bagel/42_python_modules)

## Skills Developed

| Area | Experience |
| --- | --- |
| **C and systems programming** | Pointers, memory allocation, file descriptors, static libraries, Makefiles |
| **Algorithms** | Sorting, complexity analysis, stack operations, DFS/BFS, shortest paths |
| **Python engineering** | OOP, decorators, typing, package management, validation |
| **Linux and security** | Debian administration, SSH, UFW, users/groups, `sudo` |
| **Development workflow** | Git, debugging, code review, testing, documentation, peer evaluation |

## About This Portfolio

This repository serves as an overview rather than a duplicate of the individual projects. Each linked repository contains its own source code and, where available, build and usage instructions. Some projects were completed collaboratively; contributions are described in the corresponding project documentation.

AI tools were used as learning and development aids for discussing concepts, debugging, reviewing code and requirements, and improving documentation. Project-specific usage is documented in the individual repositories.

---

*Projects completed as part of the 42 Tokyo curriculum. Portfolio maintained by [Ranran-bagel](https://github.com/Ranran-bagel).*
