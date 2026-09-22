# ⚡ Ultimate Terminal Cheatsheet

A practical terminal reference for developers.

This guide covers the **essential software required to use this cheatsheet effectively** on:

* 🪟 Windows + WSL 2
* 🍎 macOS
* 🐧 Linux

The goal is to keep the setup **clean and minimal** — only install software that is genuinely useful for everyday development and terminal work.

---

# 📋 Table of Contents

* [Required Software](#-required-software)
* [Windows + WSL 2 Setup](#-windows--wsl-2-setup)
* [Linux Setup](#-linux-setup)
* [macOS Setup](#-macos-setup)
* [Git](#-git)
* [Node.js + npm](#-nodejs--npm)
* [Docker](#-docker)
* [VS Code](#-vs-code)
* [Cursor](#-cursor)
* [Google Chrome](#-google-chrome)
* [Essential Terminal Utilities](#-essential-terminal-utilities)
* [SSH](#-ssh)
* [Verify Everything](#-verify-everything)
* [Final Checklist](#-final-checklist)

---

# 🧰 Required Software

These are the only tools this setup requires.

| Software        | Purpose                 | Windows | macOS | Linux |
| --------------- | ----------------------- | :-----: | :---: | :---: |
| WSL 2           | Linux environment       |    ✅    |   —   |   —   |
| Ubuntu          | Linux distribution      |    ✅    |   —   |   —   |
| Git             | Version control         |    ✅    |   ✅   |   ✅   |
| Node.js         | JavaScript runtime      |    ✅    |   ✅   |   ✅   |
| npm             | Node package manager    |    ✅    |   ✅   |   ✅   |
| Docker          | Containers              |    ✅    |   ✅   |   ✅   |
| VS Code         | Code editor             |    ✅    |   ✅   |   ✅   |
| Cursor          | AI code editor          |    ✅    |   ✅   |   ✅   |
| Chrome          | Web development/testing |    ✅    |   ✅   |   ✅   |
| curl            | HTTP requests           |    ✅    |   ✅   |   ✅   |
| wget            | File downloads          |    ✅    |   ✅   |   ✅   |
| jq              | JSON processing         |    ✅    |   ✅   |   ✅   |
| zip/unzip       | Archives                |    ✅    |   ✅   |   ✅   |
| build-essential | Build/compile tools     |   WSL   |   —   |   ✅   |
| SSH             | Remote server access    |   WSL   |   ✅   |   ✅   |

> **Note:** Windows users should perform terminal-based development inside **WSL 2 + Ubuntu**.

---

# 🪟 Windows + WSL 2 Setup

Windows users should use WSL 2 to get a real Linux development environment.

## 1. Open PowerShell as Administrator

Search for:

```text
PowerShell
```

Right-click:

```text
Run as administrator
```

---

## 2. Install WSL

Run:

```powershell
wsl --install
```

This installs WSL 2 and Ubuntu.

Restart your computer if Windows asks you to.

---

## 3. Open Ubuntu

After restarting, open:

```text
Ubuntu
```

from the Start menu.

Or run:

```powershell
wsl
```

---

## 4. Create Your Linux User

Ubuntu will ask:

```text
Enter new UNIX username:
```

Enter your username.

Then create a password.

> When entering your Linux password, nothing will appear on the screen. This is normal.

---

## 5. Update Ubuntu

Inside Ubuntu:

```bash
sudo apt update
sudo apt upgrade -y
```

---

## 6. Install Essential Linux Tools

Run:

```bash
sudo apt install -y \
git \
curl \
wget \
jq \
zip \
unzip \
build-essential \
openssh-client
```

---

## 7. Verify WSL

From PowerShell:

```powershell
wsl --version
```

Check your distribution:

```powershell
wsl --list --verbose
```

You should see something similar to:

```text
NAME      STATE     VERSION
Ubuntu    Running   2
```

---

# 🐧 Linux Setup

For Ubuntu/Debian-based Linux distributions:

## 1. Update the system

```bash
sudo apt update
sudo apt upgrade -y
```

---

## 2. Install Essential Tools

```bash
sudo apt install -y \
git \
curl \
wget \
jq \
zip \
unzip \
build-essential \
openssh-client
```

---

# 🍎 macOS Setup

macOS already includes many basic Unix utilities.

For a clean developer setup, install **Homebrew** first.

## 1. Install Homebrew

Install Homebrew using its official installation instructions.

Verify:

```bash
brew --version
```

---

## 2. Install Essential CLI Tools

```bash
brew install \
git \
node \
curl \
wget \
jq
```

Install Docker:

```bash
brew install --cask docker
```

---

# 🔧 Git

Git is essential for version control.

## Check Git

```bash
git --version
```

Example:

```text
git version 2.x.x
```

---

## Configure Git

Set your username:

```bash
git config --global user.name "Your Name"
```

Set your email:

```bash
git config --global user.email "your@email.com"
```

Check:

```bash
git config --global --list
```

---

# 🟢 Node.js + npm

Node.js allows JavaScript to run outside the browser.

npm is Node.js's package manager.

---

## Check Node.js

```bash
node --version
```

## Check npm

```bash
npm --version
```

Both should return version numbers.

---

## Test Node.js

Create a file:

```bash
touch test.js
```

Open it:

```bash
code test.js
```

Add:

```javascript
console.log("Node.js works!");
```

Run:

```bash
node test.js
```

Expected:

```text
Node.js works!
```

---

# 🐳 Docker

Docker is used to run applications inside containers.

Install Docker Desktop on:

* Windows
* macOS

Linux users can install Docker Engine using their distribution's official Docker installation instructions.

---

## Check Docker

```bash
docker --version
```

Check Docker Compose:

```bash
docker compose version
```

---

## Test Docker

```bash
docker run hello-world
```

If Docker is working, Docker will print a successful hello-world message.

---

## Basic Docker Commands

Show running containers:

```bash
docker ps
```

Show all containers:

```bash
docker ps -a
```

Show images:

```bash
docker images
```

Pull an image:

```bash
docker pull nginx
```

Run a container:

```bash
docker run nginx
```

Stop a container:

```bash
docker stop <container>
```

Remove a container:

```bash
docker rm <container>
```

Remove an image:

```bash
docker rmi <image>
```

---

# 💻 VS Code

VS Code is the main general-purpose code editor.

Install VS Code for your operating system.

---

## Windows + WSL

Install the **WSL extension** in VS Code.

Then from Ubuntu:

```bash
code .
```

This opens the current Linux directory in VS Code.

---

## Test

```bash
mkdir test-project
cd test-project
code .
```

---

# 🤖 Cursor

Cursor is an AI-powered code editor.

Install Cursor for your operating system.

You can open a project from the terminal using:

```bash
cursor .
```

If `cursor` is not recognized, enable the Cursor shell command from Cursor's command palette.

---

# 🌐 Google Chrome

Chrome is essential for modern web development.

It is used for:

* Testing websites
* JavaScript debugging
* Network inspection
* Console debugging
* HTML/CSS inspection
* React development
* DevTools

---

## Open Chrome DevTools

Windows/Linux:

```text
F12
```

or:

```text
Ctrl + Shift + I
```

macOS:

```text
Command + Option + I
```

---

# 🛠️ Essential Terminal Utilities

These commands are included because they are commonly required when working with development projects.

---

## curl

Used to make HTTP requests.

Check:

```bash
curl --version
```

Example:

```bash
curl https://example.com
```

API example:

```bash
curl https://api.example.com/users
```

---

## wget

Used to download files.

Check:

```bash
wget --version
```

Example:

```bash
wget https://example.com/file.zip
```

---

## jq

Used to read and manipulate JSON from the terminal.

Check:

```bash
jq --version
```

Example:

```bash
echo '{"name":"John","age":20}' | jq
```

Get one property:

```bash
echo '{"name":"John"}' | jq '.name'
```

---

## zip

Create a ZIP archive:

```bash
zip archive.zip file.txt
```

Create a ZIP from a directory:

```bash
zip -r project.zip project/
```

---

## unzip

Extract a ZIP file:

```bash
unzip archive.zip
```

---

# 🔐 SSH

SSH is essential for connecting to remote Linux servers.

Check:

```bash
ssh -V
```

Connect to a server:

```bash
ssh username@server-ip
```

Example:

```bash
ssh ubuntu@203.0.113.10
```

---

## Generate an SSH Key

```bash
ssh-keygen -t ed25519
```

Press Enter to accept the default location.

Your key will normally be stored at:

```text
~/.ssh/id_ed25519
```

---

# 🔨 Build Tools

Linux development sometimes requires compiling native dependencies.

Ubuntu/Debian:

```bash
sudo apt install build-essential -y
```

This provides tools such as:

```text
gcc
g++
make
```

Check:

```bash
gcc --version
g++ --version
make --version
```

---

# ✅ Verify Everything

Run these commands after completing the setup.

### Git

```bash
git --version
```

### Node.js

```bash
node --version
```

### npm

```bash
npm --version
```

### Docker

```bash
docker --version
```

### Docker Compose

```bash
docker compose version
```

### curl

```bash
curl --version
```

### wget

```bash
wget --version
```

### jq

```bash
jq --version
```

### SSH

```bash
ssh -V
```

### GCC

```bash
gcc --version
```

---

# 🚀 Complete Environment Test

You can quickly check your development environment with:

```bash
echo "===== Git ====="
git --version

echo "===== Node.js ====="
node --version

echo "===== npm ====="
npm --version

echo "===== Docker ====="
docker --version

echo "===== Docker Compose ====="
docker compose version

echo "===== curl ====="
curl --version

echo "===== wget ====="
wget --version

echo "===== jq ====="
jq --version

echo "===== SSH ====="
ssh -V

echo "===== GCC ====="
gcc --version
```

---

# 📦 Final Checklist

## Windows

```text
☐ WSL 2
☐ Ubuntu
☐ Git
☐ Node.js
☐ npm
☐ Docker Desktop
☐ VS Code
☐ VS Code WSL extension
☐ Cursor
☐ Google Chrome
☐ curl
☐ wget
☐ jq
☐ zip/unzip
☐ build-essential
☐ SSH
```

## macOS

```text
☐ Homebrew
☐ Git
☐ Node.js
☐ npm
☐ Docker
☐ VS Code
☐ Cursor
☐ Google Chrome
☐ curl
☐ wget
☐ jq
☐ zip/unzip
☐ SSH
```

## Linux

```text
☐ Git
☐ Node.js
☐ npm
☐ Docker
☐ VS Code
☐ Cursor
☐ Google Chrome
☐ curl
☐ wget
☐ jq
☐ zip/unzip
☐ build-essential
☐ SSH
```

---

# 🏁 You're Ready

Once the checklist is complete, you have the essential environment required for the **Ultimate Terminal Cheatsheet**.

Your basic development stack is:

```text
              TERMINAL
                  │
        ┌─────────┴─────────┐
        │                   │
      Linux             macOS
        │
      WSL 2
        │
   ┌────┴─────┐
   │          │
  Git       Node.js
   │          │
GitHub      npm
              │
          ┌───┴───┐
          │       │
       Docker   Browser
          │       │
          └───┬───┘
              │
       VS Code / Cursor
              │
          Development
```

**Keep this README as the setup guide and use the Ultimate Terminal Cheatsheet itself as the command reference.**
