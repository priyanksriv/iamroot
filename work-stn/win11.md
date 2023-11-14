## Windows 11

#### Basic Installs

- Notepad++

- Google Chrome

- MarkText Editor

- Slack for Desktop (optional)

- Cisco Anyconnect (optional)

#### Dev Installs

- Git, SSH Keygen ([refer](https://connkat.medium.com/setting-up-multiple-ssh-keys-on-one-computer-75f068d972d9) for multiple keys)

- Visual Studio Code

- Docker Desktop

- Draw.io App

- Python 3.x

- IntelliJ Idea (optional)

#### Special Instructions

- **Add Win User to Docker users' group**
  
  Follow this [FAQ for Windows](https://docs.docker.com/desktop/faqs/windowsfaqs/#why-do-i-see-the-docker-desktop-access-denied-error-message-when-i-try-to-start-docker-desktop) and if that doesn't work, then the [Youtube video](https://www.youtube.com/watch?v=LFZDUnmtTv4) shows how to add Win user to `docker-users` group using *powershell*.
  
  ```powershell
  ########  Run Powershell as admin  ########
  
  # Verify the name of the dockers-users group
  > get-LocalGroup | ft Name | findstr 'docker-users'
  
  # Add user to group
  > $user=whoami; net localgroup docker-users $user
  
  # Verify the user is added to group
  > whoami /groups | findstr 'docker-users'
  
  ########  Restart system, launch docker-dektop  ########
  ```

- **Add Python to Env Vars**
  
  Follow [this article](https://medium.com/@viknesh2798/how-to-fix-the-issues-while-using-python-command-in-the-command-prompt-ba56d9018c5f) on fixing isses with Python command-promt if it's not in path:
  
  ```
  # Win search "edit the system env variables" and click on Environment Variables
  # In section "System Variables", click on "Path" and then "Edit"
  # Add Python paths, by clicking on "New":
    C:\Program Files\Python310\
    C:\Program Files\Python310\Scripts\
    C:\Users\prisrivastav\AppData\Roaming\Python\Scripts\
  # Save/Apply
  ```

#### VS Code Customization

- Enable Dark Mode

- **Themes**: `moonlight`, `ariake dark`, `vs-code icons`, `material icons`
  
  Current: `moonlight italic` + `vs-code icons`

- **Settings**:
  
  - Font Family: Add Cascadia - in text field replace with `'Cascadia Code', Consolas, 'Courier New', monospace`
  
  - Font Size: 14 (with cascadia, change as per font)
  
  - Line Height: 1.65 (1-8 is factor-based, 8+ is absolute)
  
  - Minimap: hidden

- **Dev Extensions**
  
  - *Remote Dev* - MS: bundles includes *WSL*, *Remote Tunnels*, *Remote SSH*
  - *Docker* - MS
  - *Eclipse Keymap* - Alphabot Security

- **Python Extensions**
  
  - *Python* - MS: python-dev extension bundle
  - *Even Better TOML* - tamasfe

#### Things to Do

- Review *Startup Apps* and remove most like Teams, Slack, Docker and OneDrive.

- Make *Microsoft Terminal* the default terminal app.

- Customize *MS Edge* - themes, layout, search, toolbar apps, download location; disable rewards, sidebar apps, etc.

- Remove Edge tabs from *Alt-Tab* [navigation](https://www.majorgeeks.com/content/page/alt_tab_edge.html).

- Customize *Google Chrome* - themes, layout, search, download location; disable "Allow Chrome sign-in".
