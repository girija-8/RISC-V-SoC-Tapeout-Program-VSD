# OpenLane Setup

This repository contains scripts, instructions, and configurations to set up OpenLane on Ubuntu with Docker and all required dependencies. It is intended to make the setup process reproducible and easy to follow.

---

## Prerequisites

Before proceeding, verify that all required tools are installed and available in your PATH:

| Dependency          | Check Command                | Purpose                                  |
|---------------------|-------------------------------|------------------------------------------|
| Git                 | `git --version`               | Clone and manage repositories            |
| Docker              | `docker --version`            | Run OpenLane container environment       |
| Python 3            | `python3 --version`           | Required for OpenLane scripts and tools   |
| pip (Python pkg)     | `python3 -m pip --version`   | Python package manager                   |
| Make                | `make --version`              | Build automation for OpenLane workflows   |
| venv (Python env)    | `python3 -m venv -h`         | Create isolated Python environments      |

---

## 1. System Update & Dependencies (Required)
~~~
sudo apt update && sudo apt upgrade -y
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common gnupg lsb-release
~~~
## 2.Docker's Installation
~~~
# Add Docker's official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Set up the Docker repository
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Update apt package index
sudo apt update

# Install Docker Engine, CLI, and containerd
sudo apt install -y docker-ce docker-ce-cli containerd.io

# Install Docker Compose & Buildx plugins (important for modern Docker)
sudo apt install -y docker-buildx-plugin docker-compose-plugin

# Test Docker (needs sudo until we fix permissions)
sudo docker run hello-world

# Create docker group if it doesn't exist
sudo groupadd docker || true

# Add current user to docker group (so we can run docker without sudo)
sudo usermod -aG docker $USER

# Enable Docker service on boot
sudo systemctl enable docker
sudo systemctl start docker

# Reboot to apply group changes OR run newgrp docker to skip reboot
sudo reboot
~~~
## 3. Testing
docker run hello-world
