# Minishell  

A UNIX shell that emulates **BASH** behavior. Created in collaboration with **[@Kirkram](https://github.com/kirkram)** and **[@Welhox](https://github.com/Welhox)**.  

![Minishell Demo](https://github.com/user-attachments/assets/0413a4d6-1623-4542-91eb-4e6b0c3bfa47)  

---

## 📌 Table of Contents  

- [About the Project](#about-the-project)  
- [Features](#features)  
- [Built-in Commands](#built-in-commands)  
- [Installation & Compilation](#installation--compilation)  
- [Usage](#usage)  
- [Example Usage](#example-usage)  
- [Troubleshooting](#troubleshooting)  
- [Contributors](#contributors)  

---

## 🛠️ About the Project  

**Minishell** is a lightweight UNIX shell that mimics **BASH** behavior. It supports:  

- **Command execution** with arguments  
- **Pipes (`|`)** to chain commands  
- **Redirections (`<`, `<<`, `>`, `>>`)**  
- **Environment variable handling (`$VAR`)**  
- **POSIX signal handling**  

The project was divided into two main parts:  
- **[@Welhox](https://github.com/Welhox)** handled **parsing**  
- **[@Kirkram](https://github.com/kirkram)** focused on **execution**  

We also implemented several **built-in commands** for efficiency.  

---

## ✨ Features  

✔️ **Command Execution** – Supports absolute & relative paths  
✔️ **Pipes (`|`)** – Execute multiple commands in a single line  
✔️ **Redirections (`<`, `<<`, `>`, `>>`)** – Handle file input/output  
✔️ **Environment Variables (`$VAR`)** – Expand shell variables  
✔️ **Signal Handling** – Manage `CTRL+C`, `CTRL+D`, `CTRL+\`  
✔️ **Built-in Commands** – Custom implementations of key shell commands  

---

## 🔧 Built-in Commands  

We implemented the following **BASH built-in commands**:  

| Command | Description |
|---------|------------|
| `cd` | Change the working directory |
| `pwd` | Print the current directory |
| `export` | Set environment variables |
| `unset` | Remove environment variables |
| `env` | Display all environment variables |
| `echo` | Print text to the terminal |
| `exit` | Exit the shell |

Other commands are executed using the **execve()** system call.  

---

## ⚙️ Installation & Compilation  

### 📥 Clone the Repository  

```bash
git clone https://github.com/Welhox/minishell.git
cd minishell
```

### 🛠️ Compile the Project  

```bash
make
```

This will generate the `minishell` executable.  

---

## 🖥️ Usage  

Run **Minishell** by executing:  

```bash
./minishell
```

You can now enter commands just like in BASH!  

### 🔹 Running a Command  

```sh
minishell$ ls -l
```

### 🔹 Using Pipes  

```sh
minishell$ cat file.txt | grep "keyword"
```

### 🔹 Redirecting Output  

```sh
minishell$ echo "Hello, World!" > output.txt
```

### 🔹 Using Environment Variables  

```sh
minishell$ export NAME="Minishell"
minishell$ echo $NAME
```

### 🔹 Handling Signals  

- `CTRL+C` – Interrupts the current command  
- `CTRL+D` – Exits the shell  
- `CTRL+\` – Kills running processes  

---

## 🛠️ Troubleshooting  

### ❓ Command Not Found  
If you see:  
```
command not found
```
Make sure the command exists and is in your `$PATH`.  

### ❓ Shell Doesn't Start  
Ensure you compiled it properly with `make` and have **readline** installed.  

On **Debian-based systems** (Ubuntu):  
```bash
sudo apt install libreadline-dev
```

On **MacOS** (Homebrew):  
```bash
brew install readline
```

---

## 👥 Contributors  

- **[@Welhox](https://github.com/Welhox)**  
- **[@Kirkram](https://github.com/kirkram)**  
