# MiniBash  

A UNIX shell that emulates **BASH** behavior. Created in collaboration with **[@Kirkram](https://github.com/kirkram)**.

![Minishell Demo](https://github.com/user-attachments/assets/0413a4d6-1623-4542-91eb-4e6b0c3bfa47)  

---

## 📌 Table of Contents  

- [About the Project](#about-the-project)  
- [Features](#features)  
- [Built-in Commands](#built-in-commands)  
- [Installation & Compilation](#installation--compilation)  
- [Usage](#usage)  
- [Contributors](#contributors)  

---

## 🛠️ About the Project  

**MiniBash** is a lightweight UNIX shell that mimics **BASH** behavior. It supports:  

- **Command execution** with arguments  
- **Pipes (`|`)** to chain commands  
- **Redirections (`<`, `<<`, `>`, `>>`)**  
- **Environment variable handling (`$VAR`)**  
- **POSIX signal handling**  

The project was divided into two main parts:  
- **[@Welhox](https://github.com/Welhox) (Me)** handled **parsing**  
- **[@Kirkram](https://github.com/kirkram)** focused on **execution**  

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

### 🛠️ Install Dependencies  

Ensure you have the **readline** library installed before compiling:  

On **Debian-based systems** (Ubuntu):  
```bash
sudo apt install libreadline-dev
```

On **MacOS** (Homebrew):  
```bash
brew install readline
```

### 🔨 Compile the Project  

```bash
make
```

This will generate the `minishell` executable.  

---

## 🖥️ Usage  

Run **MiniBash** by executing:  

```bash
./minishell
```

You can now enter commands just like in BASH!  

---

## 👥 Contributors  

- **[@Welhox](https://github.com/Welhox)**  
- **[@Kirkram](https://github.com/kirkram)**  
