# Shell Implementation in C

## Author
**Shriya Kansal**

---

## Overview

This project is a custom Unix-like shell implemented in **C**, developed as part of a systems programming course.  
The shell replicates core functionalities of standard Unix shells while introducing several custom-built commands.

It supports command parsing, foreground and background process execution, signal handling, logging, and multiple built-in utilities implemented from scratch.

---

## Features

- Interactive shell prompt
- Execution of external commands using `fork`, `exec`, and `wait`
- Foreground and background process handling
- Signal handling for process control
- Command logging
- Modular design with separate source and header files
- Custom built-in commands implemented as part of the shell

---

## Supported Built-in Commands

- **hop**  
  Navigate directories with support for relative and absolute paths.

- **reveal**  
  Display directory contents with optional flags.

- **seek**  
  Search for files and directories recursively.

- **ping**  
  Send signals to processes using PID.

- **proclore**  
  Display detailed information about a given process.

- **fg / bg**  
  Manage foreground and background jobs.

- **log**  
  Maintain a log of executed commands.

- **neonate**  
  Monitor newly created processes at fixed intervals.

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

- Modular implementation with clear separation between functionality
- Extensive use of system calls such as `fork()`, `execvp()`, `waitpid()`, and `kill()`
- Robust signal handling for background and foreground job control
- Error handling for invalid commands and arguments

## Future Improvements

- Command piping and redirection
- Auto-completion support
- Enhanced job control utilities
- Improved error messaging and debugging support

## Notes

This project was developed for academic purposes and focuses on understanding low-level system interactions and shell design principles.
