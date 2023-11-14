### WSL2 (with Ubuntu 22.04)

#### Install Windows Subsystem for Linux (WSL 2)

- Installation - run *Powershell as Admin*; restart is required as install enables WSL too:
  
  ```bash
  # View list of supported distributions
  $ wsl --list --online
  
  # Insall Ubuntu 22.04 using the distro name from the list above
  $ wsl --install Ubuntu-22.04
  
  # Create user with username `iamroot` and add a password; Update.
  $ sudo apt update && sudo apt upgrade
  ```

- Moving to non-system partition (optional) - todo

- Make Ubuntu the default profile in *MS Terminal*, go to "Settings" > "Startup".

#### Pre-configuration

- Install, if absent: `vim`
  
  ```bash
  $ sudo apt install vim -y
  ```

- Open *MS Terminal* and edit [WSL config](https://learn.microsoft.com/en-us/windows/wsl/wsl-config):
  
  ```bash
  # Open WSL Config file inside Ubuntu
  $ sudo vim /etc/wsl.conf
  
  # Ensure the contents and save
  [boot]
  systemd=true
  
  [interop]
  enabled=true
  
  [user]
  default=iamroot
  ```

- Create directories in `home` folder
  
  ```bash
  $ cd ~/
  $ mkdir data downloads  # any other dirs req.
  ```

- Add *alias* in Ubuntu to any desired Windows location (like user home):
  
  ```bash
  # open bashrc
  $ vim ~/.bashrc
  # add alias
  alias cdwin='cd /mnt/c/Users/prisrivastav/'  # or 'cd /mnt/d/priyanksriv/'
  ```

#### Basic Installs

- Install, if absent: `tree`, `htop`, `curl`, `wget`, `ca-certificates`, `jq`
  
  ```bash
  $ sudo apt install <package> -y
  ```

- Install `bat` -- a better `cat` -- follow [instructions](https://www.linode.com/docs/guides/how-to-install-and-use-the-bat-command-on-linux/#how-to-install-bat) and add [alias](https://askubuntu.com/a/1444283) `bcat`:
  
  ```bash
  # install
  $ sudo apt install bat
  
  # open bashrc
  $ vim ~/.bashrc
  # add alias
  alias bcat='batcat'
  ```

- Install `PDFtk` (todo)

- Install `Thunar` window manager (optional)
  
  ```bash
  $ sudo apt install thunar -y
  ```

#### Post-configuration

- USB support in WSL via [USBIPD-WIN](https://learn.microsoft.com/en-us/windows/wsl/connect-usb#install-the-usbipd-win-project) - todo

- Interop: File [Systems](https://learn.microsoft.com/en-us/windows/wsl/filesystems), [Permissions](https://learn.microsoft.com/en-us/windows/wsl/file-permissions) and [Ownership](https://devblogs.microsoft.com/commandline/chmod-chown-wsl-improvements/) - todo

- Interop: [Networking](https://learn.microsoft.com/en-us/windows/wsl/networking) - todo

#### Dev Installs

- Install, if absent: `git`, `ssh`; configure ssh (`ssh-keygen`). Configure `git` username and email (global).

- [HTTPie](https://httpie.io/docs/cli/debian-and-ubuntu) - terminal API client

- Neovim

- Java 11 (OpenJDK)

#### Python Dev

- Python 3.x
  
  ```bash
  # check version
  $ python3 --version
  
  # update, if required
  $ sudo apt install python3.10 #verify if python3 now symlinks to latest
  ```

- Virtual Env
  
  ```bash
  $ sudo apt install python3.10-venv
  ```

- Poetry - [install](https://python-poetry.org/docs/#installation) specific version
  
  ```bash
  # Installs at `~/.local/bin` which is in path via `~/.profile`
  $ curl -sSL https://install.python-poetry.org | POETRY_VERSION=1.2.0 python3 -
  ```

- Pyenv, Poetry - [new project](https://www.youtube.com/watch?v=547Jr26duHQ).

#### Configure VS Code and Docker WSL Integration

- **Visual Studio Code**
  
  - [Setup](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode) Win *VS Code* for WSL (via extension, remote VS Code server)
  
  - References: [Usage](https://code.visualstudio.com/docs/remote/wsl) *VS Code* with WSL, [Remote Dev](https://code.visualstudio.com/docs/remote/troubleshooting) in *VS Code*
  
  - IMP: Open a project in *VS Code* from WSL and then go to "Python" extensions to enable/install it for WSL Env. [Refer](https://armand-sauzay.medium.com/python-project-setup-a-step-by-step-guide-to-industry-best-practices-dbce717b2d12) for creating a simple python project with WSL + *VS Code*.

- **Docker Desktop**
  
  - [Enabling](https://docs.docker.com/desktop/wsl/) *Docker* WSL Integration.
  
  - Further [reading](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2#_using-vs-code), *Docker* + WSL2 + VS Code

#### Troubleshooting

- Scrolling inside Vim - todo

- Disabling terminal sound/buzzer - todo
