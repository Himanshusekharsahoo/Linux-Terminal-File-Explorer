# 🗂️ Linux Terminal-Based File Explorer( Capstone Project )

## 📘 Overview
This project is a **console-based File Explorer written in C++** that runs exclusively on **Linux operating systems**. It allows users to **navigate directories**, **view file details**, and **perform basic file management operations** directly through the terminal interface.

This application was developed as the **Capstone Project for the Linux Operating System (LinuxOS) course**.

---

## 🎯 Objective
The primary objective was to develop a **C++ file explorer** that interacts directly with the **Linux file system** using system calls. Key features include:
* Viewing detailed file information (similar to `ls -l`)
* Intuitive keyboard-controlled directory navigation
* Performing essential file operations (copy, move, rename, delete, search)
* Providing an efficient and text-based file management solution.

---

## ⚙️ Features

### 🖥️ Normal Mode
The application starts in **Normal Mode**, which is dedicated to exploring and navigating the file system.

#### Displayed File Details:
* **File / Directory Name**
* **Permissions** (e.g., `-rw-r--r--`)
* **Owner & Group**
* **File Size**
* **Last Modified Time**

#### Navigation Controls:
| Key | Action |
| :---: | :--- |
| `↑` / `↓` | Move cursor up/down in the file list |
| `Enter` | Open selected file or directory |
| `Backspace` | Move one level up (parent directory) |
| `h` | Go directly to the **Home** directory |
| `←` | Go to the previously visited directory (Back) |
| `→` | Go forward to a recently visited directory |

#### Example Screenshot (Normal Mode):
![Normal Mode Screenshot](images/normal_mode.png)

---

### 💬 Command Mode
Pressing the **`:`** key transitions the application into **Command Mode**. In this mode, users can type powerful commands for file and directory manipulation.

#### Supported Commands:

| Command | Description |
| :--- | :--- |
| `copy <src1> <src2> ... <destination>` | Copy specified files and/or directories to a destination |
| `move <src1> <src2> ... <destination>` | Move specified files and/or directories to a destination |
| `rename <old_name> <new_name>` | Rename a specific file or directory |
| `create_file <file_name> <path>` | Create a new file at the specified path |
| `create_dir <dir_name> <path>` | Create a new directory at the specified path |
| `delete_file <path>` | Permanently delete a file |
| `delete_dir <path>` | Recursively delete a directory and all its contents |
| `goto <directory_path>` | Navigate directly to a specific directory path |
| `search <file_name>` | Search for a file or directory by name within the current path |
| `ESC` | Exit Command Mode and return to Normal Mode |

#### Example Screenshot (Command Mode):
![Command Mode Screenshot](images/cmd_mode.png)

---

## 🧩 Technical Implementation

* **Language:** C++
* **Compiler:** `g++`
* **Build System:** `Makefile`

### Libraries Used (Linux System Calls):
* `<dirent.h>` – for reading and handling directory contents
* `<sys/stat.h>` – for retrieving file metadata and permissions
* `<unistd.h>` – for navigation and system interaction
* `<termios.h>` – for non-canonical terminal key handling (reading single keystrokes)
* `<pwd.h>`, `<grp.h>` – for translating user/group IDs to names

---

## 🚀 How to Compile and Run (on Linux)

### Prerequisites
Ensure your Linux system has the following installed:
* **g++ compiler**
* **make utility**

### Steps
1.  **Install dependencies** (if not already present):
    ```bash
    sudo apt update
    sudo apt install g++ make -y
    ```

2.  **Navigate** to the project folder:
    ```bash
    cd Linux-Terminal-Based-File-Explorer
    ```

3.  **Build** the project using the `Makefile`:
    ```bash
    make
    ```

4.  **Run** the file explorer:
    ```bash
    ./main
    ```

To clean all generated executable files and object files:

make clean
---
## 🧠 Learning Outcomes
This capstone project provided valuable experience in:

* Interfacing directly with the **Linux file system** using low-level **system calls** (`open`, `read`, `write`, `stat`, etc.).
* Implementing **terminal control** and handling **keyboard-based input** for an interactive console application (using libraries like `<termios.h>`).
* Developing robust **file and directory management** features in C++ (copy, move, delete, etc.).
* Organizing and managing a larger, multi-file project efficiently using a **Makefile**.

---

## 🧑‍💻 Author
**Name:** Himanshu sekhar sahoo 
**Course:** B.Tech – Computer Science & Engineering  
**Subject:** Linux Operating System (LinuxOS) Capstone Project  
**Date:** November 2025
