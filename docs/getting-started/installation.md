# Installation Guide

This guide will walk you through setting up your environment for the GenAI Docker Workshop.

## 1. Docker Installation

Docker is the primary platform we'll use throughout this workshop. Follow these steps to install Docker based on your operating system.

### Windows

1. **System Requirements**:
   - Windows 10 64-bit: Pro, Enterprise, or Education (Build 17763 or later)
   - Enable Hyper-V and Containers Windows features

2. **Installation Steps**:
   - Download Docker Desktop from [Docker's website](https://www.docker.com/products/docker-desktop)
   - Run the installer and follow the prompts
   - After installation, Docker Desktop will start automatically

### macOS

1. **System Requirements**:
   - macOS must be version 10.15 or newer
   - For Apple Silicon Macs, ensure you have Rosetta 2 installed

2. **Installation Steps**:
   - Download Docker Desktop from [Docker's website](https://www.docker.com/products/docker-desktop)
   - Drag the Docker icon to the Applications folder
   - Start Docker from the Applications folder

### Linux

For Linux, you'll install Docker Engine directly:

```bash
# Update package index
sudo apt-get update

# Install prerequisites
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release

# Add Docker's official GPG key
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg

# Set up the stable repository
echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

# Install Docker Engine
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

# Add your user to the docker group to run docker without sudo
sudo usermod -aG docker $USER
```

**Note**: You may need to log out and back in for the group changes to take effect.

## 2. Model Runner Installation

Model Runner is a specialized Docker component for running GenAI models efficiently. Here's how to install it:

```bash
# Pull the Model Runner image
docker pull docker/genai-model-runner:latest

# Verify the installation
docker run --rm docker/genai-model-runner:latest --version
```

## 3. MCP Toolkit Installation

The MCP (Model Container Platform) Toolkit helps manage containerized AI models:

```bash
# Pull the MCP Toolkit image
docker pull docker/mcp-toolkit:latest

# Set up MCP CLI
docker run --rm -v /usr/local/bin:/target docker/mcp-toolkit:latest install
```

## 4. Workshop Environment Setup

Set up the workshop environment by cloning the repository and installing dependencies:

```bash
# Clone the workshop repository
git clone https://github.com/collabnix/genai-docker-workshop.git
cd genai-docker-workshop

# Clone lab repositories
git clone https://github.com/ajeetraina/genai-model-runner-metrics.git
git clone https://github.com/ajeetraina/catalog-service-demo.git
```

## 5. Verify Installation

Verify that everything is installed correctly:

```bash
# Check Docker
docker --version

# Test Docker with a simple container
docker run hello-world

# Check Model Runner
docker run --rm docker/genai-model-runner:latest --version

# Check MCP Toolkit
mcp --version  # If you installed the CLI
```

If all commands run without errors, your environment is set up correctly!

## 6. Docker Compose Installation (If Not Included)

Docker Compose should be included with Docker Desktop. If you're on Linux and need to install it separately:

```bash
# Install Docker Compose
sudo curl -L "https://github.com/docker/compose/releases/download/v2.18.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose

# Verify the installation
docker-compose --version
```

## Troubleshooting

If you encounter any issues during installation:

1. **Docker fails to start**:
   - On Windows, ensure Hyper-V is enabled
   - On macOS, check System Preferences for any security blocks
   - On Linux, ensure the Docker daemon is running: `sudo systemctl start docker`

2. **Permission issues**:
   - On Linux, ensure your user is added to the docker group and you've logged out and back in

3. **Network issues**:
   - Check your firewall settings
   - Ensure Docker can access the internet for pulling images

For any other issues, refer to the [Docker documentation](https://docs.docker.com/) or reach out to the workshop facilitators.

## Next Steps

Now that you have installed all the necessary components, you're ready to dive into the [GenAI Fundamentals](../genai-fundamentals/overview.md)!
