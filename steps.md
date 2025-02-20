# Steps:
This document provides a simple guide to setup Docker, Ollama, and OpenWebUI, to host a Deepseek Instance accessible on your local network.

## Step 1. Setting Up Docker:
You can follow the docker [Install Guide](https://docs.docker.com/engine/install/), for this setup I started with installing Docker on my gaming laptop running Fedora 41 and RPi4-4gb.

> **Note**
> You can also use the automated install script from docker with the following commands:
> ```
> curl -sSL https://get.docker.com | sh
> ```

For [Fedora](https://docs.docker.com/engine/install/fedora/):
```
sudo dnf install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

For Raspberry Pi [(32-bit OS)](https://docs.docker.com/engine/install/raspberry-pi-os/) and [(64-bit OS)](https://docs.docker.com/engine/install/debian/):
- Start by adding the appropritate repositories for apt:
  ```
  # Since this showcase is using a Raspberry Pi 4, we will use the 64-bit install
  # Add Docker's official GPG key:
  sudo apt-get update
  sudo apt-get install ca-certificates curl
  sudo install -m 0755 -d /etc/apt/keyrings
  sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
  sudo chmod a+r /etc/apt/keyrings/docker.asc
  # Add the repository to Apt sources:
  echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  sudo apt-get update
  ```
- Install the required packages:
  ```
  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
  ```
- Add the current user to the docker user group:
  > sudo usermod -aG docker $USER

  
