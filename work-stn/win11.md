## Windows 11 with WSL Ubuntu 22.04



### Windows

#### Basic Installs

- Notepad++

- Chrome Browser

- MarkText Editor

#### Dev Installs

- Git, SSH Keygen

- Visual Studio Code

- Docker Desktop

- Draw.io App

- Python 3.x

- Java 11

#### Optional Installs

- Slack

- IntelliJ (for Java)

- Cisco Anyconnect

#### Special Instructions

- Docker: Follow this [FAQ]([FAQs for Windows | Docker Docs](https://docs.docker.com/desktop/faqs/windowsfaqs/#why-do-i-see-the-docker-desktop-access-denied-error-message-when-i-try-to-start-docker-desktop)) and if that doesn't work, then the [video]([docker desktop access denied not in docker-users group - YouTube](https://www.youtube.com/watch?v=LFZDUnmtTv4)) shows how to add Win user to `docker-users` group using *powershell*.
  
  ```
  # Run Powershell as admin
  > get-LocalGroup | ft Name    # List groups
  > whoami                      # Get windows user
  > whoami /groups              # Get users' groups
  > net localgroup docker-users "<username>"
  # Restart system and launch Docker desktop
  ```
  
  

- 
