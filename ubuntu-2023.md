<div align="center">
    <h1>2023 Ubuntu Environment Set Up</h1>
    <i>A collective list of installations, preparations, and development informations and Sources for Ubuntu Environment</i>
</div>

## Index
---
1. [Plain Ubuntu](#after-ubuntu-installations) 
2. Programming Language 
   - [Python (base and latest)](#python-base-and-latest)
   - [Java (JRE and JDK)](#java-jre-and-jdk)
   - [Go](#go)
   - [R](#r)
   - [NVM (Node Version Manager)](#node-version-manager)
   - [PostgreSQL](#postgresql)
   - [LaTex]()
3. IDE
   - [vim](#vim)
   - [Guake](#guake)
   - [Visual Studio Code](#visual-studio-code)
   - [Jetbrains Tools (For PyCharm, IntelliJ Idea, GoLand, more)](#jetbrains-toolbox-on-ubuntu-2204)
   - [RStudio](#rstudio)
   - [Postman API](#postman-api)
   - [Dbreaver](#dbreaver)
   - [Docker](#docker-on-ubuntu-2204)
4. Productivity and Workflow
   - [Git and GitHub](#git-and-github)
   - [Notion](#notion)
   - [Syncthing](#syncthing)
   - [Emacs org-mode](#emacs-org-mode)
   - [Bitwarden](#bitwarden)
   - [Twilio Authy](#twilio-authy)
   - [Brave](#brave)
5. More
   - [psensor](#psensor)
   - [Discord](#discord)
   - [Microsoft Teams](#microsoft-teams)
   - [Zoom Client](#zoom-client)
   - [Spotify](#spotify)
   - [WhatsApp](#whatsapp)
   - [OBS Studio](#obs-studio)
   - [VLC](#vlc)



## After Ubuntu Installations
   - `sudo apt update`
   - `sudo apt upgrade`

## Programming Language
---
### Python (base and latest)
1. Python Base (Python 3.10.6)

2. Python Latest (Python 3.11.2)

**Resources**: https://www.debugpoint.com/install-python-3-11-ubuntu/

### Java (JRE and JDK)
1. 

**Resources**: 

### Go
1. 

**Resources**: https://go.dev/doc/install

### R
1. 

**Resources**:  

### Node Version Manager
1. 

**Resources**: https://www.javatpoint.com/install-nvm-ubuntu

### PostgreSQL
1. `sudo apt update && sudo apt upgrade`
2. `sudo apt install postgresql postgresql-contrib`
3. Start the services, `systemctl start postgresql.service`
4. Check status, `systemctl status postgresql.service`


**Resources**: https://www.youtube.com/watch?v=0Il040ExA_Q

## Integrated Development Environment (IDE)
---

### vim
1. 

**Resources**:  

### Guake
1. 

**Resources**:  

### Visual Studio Code
1. 

**Resources**:  

### Jetbrains Toolbox on Ubuntu 22.04
1. Download the zipped folder `.tar.gz` [here](https://www.jetbrains.com/toolbox-app/)
2. Open Terminal and change the directory, `cd /opt/`
3. Extract the file, `udo tar -xvzf ~/Downloads/jetbrains-toolbox-1.xx.xxxx.tar.gz`
4. You can rename the folder, `sudo mv jetbrains-toolbox-1.xx.xxxx jetbrains`
5. And then open Jetbrains Toolbox, `jetbrains/jetbrains-toolbox`
6. If there some errors from [FUSE](https://en.wikipedia.org/wiki/Filesystem_in_Userspace), just download it with these steps:
    - `sudo add-apt-repository universe`
    - `sudo apt install libfuse2`
7. And type step 5 again, and the Jetbrains Toolbox will launched. 
**Resources**:  

### RStudio
1. 

**Resources**:  

### Postman API
1. 

**Resources**:  

### Dbreaver
1. 

**Resources**: 

### Docker on Ubuntu 22.04
**A. Docker Engine**
1. if there any old versions, uninstalled it first
   - `sudo apt-get remove docker docker-engine docker.io containerd runc`
2. And now, we will start to set up the repository
   - `sudo apt-get update`
   - `sudo apt-get install ca-certificates curl gnupg lsb-release`
3. Add Docker's official GPG key
   - `sudo mkdir -m 0755 -p /etc/apt/keyrings`
   - `curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg`
4. Set up the repositories to `sources.list.d`
   - `echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`
5. Now, we can install docker engine. First, update the `apt` package
   - `sudo apt-get update`
   - if there error while receiving GPG, do this steps:
      - `sudo chmod a+r /etc/apt/keyrings/docker.gpg`
      - `sudo apt-get update`
6. Install **Docker Engine**, **containerd**, and **Docker Compose**
   - `sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`
7. Verify the installations
   - `sudo docker run hello-world`
 
**B. Docker Desktop**
1. Visit this link https://docs.docker.com/desktop/install/ubuntu/
2. Download the .deb package to your local (approxiamately 490 Mb)
3. Go to directory where the `.deb` are downloaded
4. Install the `.deb` app, just following your latest versions that already downloaded:
   - `sudo apt install ./docker-desktop-4.16.2-amd64.deb`
5. After that, you can open the Docker Desktop

### Try Sample Container
1. Go to `Container` menu and copy the sample container command for running it
   - `docker run -d -p 80:80 docker/getting-started`\
2. The Repositories for example docker image are [here](https://github.com/docker/getting-started)

**Resources**: You can check the installations video [here](https://www.youtube.com/watch?v=Vplj9b0L_1Y)


## Productivity and Workflow
---

### Git and GitHub
1. 

**Resources**: 

2.  Set UP SSH Key
- `ssh-keygen -t ed25519 -C "your_email@example.com"`
- `eval "$(ssh-agent -s)"`
- `ssh-add ~/.ssh/id_ed25519`
- `cat ~/.ssh/id_ed25519.pub`
- Go to **Settings -> Access -> SSH and GPG Keys**
- On **SSH Keys** sections, click **New SSH Key**
- Set Up th title, and input the key
- If already enable 2FA, input the authentications code.

**Resources**: [First](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent), [Second](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

### Notion
1. 

**Resources**: 

### Syncthing
1. 

**Resources**: 

### VS Code org-mode
1. 

**Resources**: https://github.com/vscode-org-mode/vscode-org-mode, [Wiki](https://github.com/vscode-org-mode/vscode-org-mode/wiki)

### Bitwarden
1. 

**Resources**: 

### Twilio Authy
1. 

**Resources**: 

### Brave
1. 

**Resources**: 


## More
---
### psensor
1. 

**Resources**: 

### Discord
1. 

**Resources**: 

### Microsoft Teams
1. 

**Resources**: 

### Zoom Client
1. 

**Resources**: 

### Spotify
1. 

**Resources**: 

### WhatsApp
1. 

**Resources**: 

### OBS Studio
1. 

**Resources**: 

### VLC
1. 

**Resources**: 