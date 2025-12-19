# Shell Implementation in C

## Author
**Shriya Kansal**

---

## Overview

This repository contains a custom Unix-style shell implemented in **C**, designed to replicate core behaviors of standard command-line shells. The shell provides an interactive environment for executing both built-in and external commands, with support for process management, signal handling, job control, and I/O operations.

The project focuses on low-level systems programming concepts and closely follows Unix process and signal semantics.

---

## Functionality Overview

The shell launches an interactive prompt and continuously waits for user input. It parses commands, determines whether they are built-in or external, and executes them accordingly.

Key capabilities include:
- Foreground and background process execution
- Command parsing and argument handling
- Signal handling for interrupts and job control
- Process inspection and management
- Input/output redirection and piping

---

## Built-in Commands and Features

### `hop`
Changes the current working directory. Supports:
- `.`
- `..`
- `~` (home directory)
- `-` (previous directory)

---

### `reveal`
Lists directory contents with support for:
- `-a` : show hidden files  
- `-l` : detailed listing  

Output is color-coded for improved readability.

---

### `log`
Maintains a history of recently executed commands. Supports:
- Viewing command history
- Executing commands from history
- Clearing stored history

---

### `proclore`
Displays information about a given process, including:
- Process ID
- Execution status
- Memory usage
- Executable path

---

### `seek`
Searches for files or directories with optional filters:
- `-d` : directories only  
- `-f` : files only  
- `-e` : exact match  

---

### `activities`
Lists currently running background processes started by the shell.

---

### `iMan`
Fetches and displays manual pages from an online source.

---

### Job Control Commands
- `fg` : Bring a background process to the foreground  
- `bg` : Resume a stopped process in the background  

---

## Job Control and Signals

The shell supports basic job control and signal handling:

- **Ctrl + C** : Interrupts the currently running foreground process  
- **Ctrl + Z** : Stops the foreground process and moves it to the background  
- **Ctrl + D** : Exits the shell after cleanup  

---

## Build Instructions

To compile the shell, run:

```bash
make
```

To start the shell:
```bash
./shell
```


## Dependencies

- GCC compiler
- POSIX-compliant operating system

## Design Highlights

- Minimal and modular C code
- Explicit and careful use of system calls
- Emphasis on correctness and clarity
- Designed for extensibility rather than production deployment

## Limitations
- No advanced shell scripting support
- Limited job control compared to full-featured shells like Bash
- No tab completion or configurable prompts
- Basic error handling

## Future Improvements

-Persistent command history across sessions
- Tab completion
- Environment variable support
- Improved diagnostics and error reporting