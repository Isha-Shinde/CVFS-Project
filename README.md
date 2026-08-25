# Customised virtual File System (CVFS)

# Project Overview

The Customised Virtual File System (CVFS) is a software-based file system developed using C programming.

The main purpose of this project is to understand how an operating system manages files internally using concepts such as:

- Boot Block
- Super Block
- Inode
- File Table
- UAREA
- UFDT
- File Descriptors
- File Permissions
- Read/Write Offsets
- Reference Counts
- Memory Management

Unlike a traditional file system that stores data on a physical disk, this project maintains the virtual file-system data in RAM.

Therefore, the files created inside CVFS are temporary and the data is lost when the program terminates.

---

# Objectives

- Understand the internal working of a file system
- Understand Inode, File Table, UAREA and UFDT
- Implement basic file operations using C
- Learn file permissions and file management

The documentation specifically identifies learning the internal working of a file system and implementing it completely in RAM as major objectives.

---

# Technologies Used

- C Programming
- Linux
- GCC Compiler
- VS Code
- Command Line Interface (CLI)

The project uses a Command Line Interface (CLI) for interacting with the virtual file system.

---

# Architecture

- Superblock: Tracks total and free inodes.
- Inode Table: Stores metadata for each file (name, size, type, permissions, etc.).
- File Table: Maintains open file state (offsets, mode, reference count).
- UFDT: Maps file descriptors to file table entries.
- Buffer: Each file has a dedicated buffer for its contents.

# Data Structures Used

- Boot Block : The `BootBlock` stores information related to booting the operating system.
- Super Block : The `SuperBlock` maintains information about the complete virtual file system.
- Inode : The Inode stores metadata related to a file.
- File Table : The File Table stores information about an opened file.
- UAREA : The `UAREA` stores information related to the currently running process.
- UFDT : It maintains references to the File Table entries of currently opened files.
  
---

# File Operations

The CVFS simulates important file-system operations.

| Operation | Purpose                          |
| --------- | -------------------------------- |
| `creat`   | Create a new virtual file        |
| `open`    | Open an existing file            |
| `read`    | Read data from a file            |
| `write`   | Write data into a file           |
| `close`   | Close an opened file             |
| `lseek`   | Change the current read position |
| `stat`    | Display file metadata            |
| `unlink`  | Delete a file                    |
| `ls`      | Display files                    |
| `help`    | Display available commands       |
| `man`     | Display command information      |
| `clear`   | Clear the terminal               |
| `exit`    | Exit CVFS                        |

# How CVFS Works

The overall flow of the project is:

Start -> Initialize Super Block
  ↓
Create / Initialize Inode List
  ↓
Initialize UAREA
  ↓
Display CVFS Prompt
  ↓
Accept User Command
  ↓
Parse Command
  ↓
Identify Required Operation
  ↓
Call Corresponding Function
  ↓
Perform File Operation
  ↓
Display Result
  ↓
Wait for Next Command
  ↓
Exit
---

# Documentation

Detailed project documentation is available in:

----
# License

This project is intended for **educational and learning purposes**.


