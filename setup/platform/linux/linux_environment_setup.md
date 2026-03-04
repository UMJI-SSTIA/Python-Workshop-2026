# Python + VS Code on Linux

This guide covers the installation and configuration of a professional Python environment on Linux (Ubuntu/Debian, Fedora, or Arch-based distros).

## 1. Install VS Code

While you can use `snap` or `flatpak`, the native package is often more stable for development.

### **Ubuntu/Debian/Mint**

```bash
sudo apt update
sudo apt install software-properties-common apt-transport-https wget
wget -q https://packages.microsoft.com/keys/microsoft.asc -O- | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://packages.microsoft.com/repos/vscode stable main"
sudo apt update
sudo apt install code
```

### **Fedora/RHEL**

```bash
sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
sudo sh -c 'echo -e "[code]\nname=Visual Studio Code\nbaseurl=https://packages.microsoft.com/pyrepos/vscode\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/vscode.repo'
sudo dnf install code
```

Or you can download it from the web page [Visual Studio Code](https://code.visualstudio.com/)

## 2. Prepare Python

Most Linux distros come with Python 3, but they often strip out the "Virtual Environment" module to save space. You'll need to add it back.

### **Install Python & Venv Tools**

* **Ubuntu/Debian:** `sudo apt install python3 python3-pip python3-venv`
* **Fedora:** `sudo dnf install python3 python3-pip` (venv is usually included)
* **Arch:** `sudo pacman -S python python-pip`

## 3. Clone Our Workshop Repo

You need to clone our github repository to get all the notebooks and scripts on your local machine. Choose a folder your like, and run the command below.

```bash
git clone https://github.com/UMJI-SSTIA/Python-Workshop-2026.git
```

Go to the workspace folder

```bash
cd Python-Workshop-2026
```

## 4. The Workflow: Virtual Environments

On Linux, it is a cardinal sin to install project libraries into your system Python. **Always use a virtual environment.**

### **Create virtual environments project**

```bash
python3 -m venv .venv
```

### **Activate it in the Terminal**

```bash
source .venv/bin/activate
```

> **Note:** Once activated, your terminal prompt will usually show `(.venv)` at the beginning.

## 5. Verification

Create a file called `test.py` with `nano` or `vim`(Here I will use nano for example):

```bash
nano test.py
```

Copy and paste the test code into the test.py, if you don't understand what this code doing, it doesn't really matter, what it does is just print your python version for verification

```python
import sys
print(f"Current Python Version: {sys.version}")
print("Environment: " + sys.prefix)
```

![illustrate](../images/test_code.png)

Save it with "ctrl+X" for exit, "Y" for save, and "Enter" to ensure the file name.

Run the code in your virtual environment

```bash
python3 test.py
```

![illustrate](../images/verification.png)

If you see something like this, congratulations！Your python environment is well-done. (Make sure the environment is .venv)

## 6. Launching VS Code

Of course, nowadays, nobody will do coding with nano or vim, so we will talk about vscode setup later in the share folder. Let's just open the vscode with simple command below!

```bash
code .
```

Now configure your VS Code

***See [vscode_setup](https://github.com/UMJI-SSTIA/Python-Workshop-2026/tree/main/setup/share/vscode_setup) inside the share folder***
