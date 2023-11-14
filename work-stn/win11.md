## Windows 11 with WSL Ubuntu 22.04

### Windows

#### Basic Installs

- Notepad++

- Google Chrome

- MarkText Editor

#### Dev Installs

- Git, SSH Keygen ([refer](https://connkat.medium.com/setting-up-multiple-ssh-keys-on-one-computer-75f068d972d9) for multiple keys)

- Visual Studio Code

- Docker Desktop

- Draw.io App

- Python 3.x

- Java 11 (OpenJDK)

#### Special Instructions

- **Add Win User to Docker users' group**
  
  Follow this [FAQ for Windows](https://docs.docker.com/desktop/faqs/windowsfaqs/#why-do-i-see-the-docker-desktop-access-denied-error-message-when-i-try-to-start-docker-desktop) and if that doesn't work, then the [Youtube video](https://www.youtube.com/watch?v=LFZDUnmtTv4) shows how to add Win user to `docker-users` group using *powershell*.
  
  ```powershell
  # Run Powershell as admin
  > get-LocalGroup | ft Name    # List groups
  > whoami                      # Get windows user
  > whoami /groups              # Get users' groups
  > net localgroup docker-users "<username>"
  # Restart system and launch Docker desktop
  ```

- **Add Python to Env Vars**
  
  Follow [this article](https://medium.com/@viknesh2798/how-to-fix-the-issues-while-using-python-command-in-the-command-prompt-ba56d9018c5f) on fixing isses with Python command-promt if it's not in path:
  
  ```
  - Win search "edit the system env variables" and click on Environment Variables.
  - In section "System Variables", click on "Path" and then "Edit".
  - Add Python paths, by clicking on "New":
    C:\Program Files\Python310\
    C:\Program Files\Python310\Scripts\
    C:\Users\prisrivastav\AppData\Roaming\Python\Scripts\
  - Save/Apply.
  ```

#### Optional Installs

- Slack for Desktop

- IntelliJ (for Java)

- Cisco Anyconnect

#### Things to Do

- Review *Startup Apps* and remove most like Teams, Slack, Docker and OneDrive.

- Make *Microsoft Terminal* the default terminal app.

- Customize *MS Edge* - themes, layout, search, toolbar apps, download location; disable rewards, sidebar apps, etc.

- Remove Edge tabs from *Alt-Tab* [navigation](https://www.majorgeeks.com/content/page/alt_tab_edge.html).

- Customize *Google Chrome* - themes, layout, search, download location; disable "Allow Chrome sign-in"
