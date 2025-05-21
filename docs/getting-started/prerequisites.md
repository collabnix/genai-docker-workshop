# Prerequisites

Before starting the GenAI Docker Workshop, please ensure you have the following prerequisites set up:

## Hardware Requirements

- **CPU**: 4+ cores recommended
- **RAM**: Minimum 8GB, 16GB+ recommended for running models locally
- **Disk Space**: At least 20GB of free space
- **GPU**: Optional but recommended for model training and faster inference (NVIDIA GPU with CUDA support)

## Software Requirements

### Required Software

1. **Docker**
   - Docker Desktop for [Windows](https://docs.docker.com/desktop/install/windows-install/) or [Mac](https://docs.docker.com/desktop/install/mac-install/)
   - Docker Engine for [Linux](https://docs.docker.com/engine/install/)
   - Docker Compose (included in Docker Desktop)
   - Verify installation with:
     ```bash
     docker --version
     docker-compose --version
     ```

2. **Git**
   - Download and install from [git-scm.com](https://git-scm.com/downloads)
   - Verify installation with:
     ```bash
     git --version
     ```

3. **Python 3.8+**
   - Download from [python.org](https://www.python.org/downloads/) or use your system's package manager
   - Verify installation with:
     ```bash
     python --version
     ```

4. **Text Editor or IDE**
   - Visual Studio Code, PyCharm, or any preferred code editor

### Optional but Recommended

1. **NVIDIA Container Toolkit** (for GPU support)
   - Install only if you have an NVIDIA GPU
   - Follow [installation instructions](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html)

2. **kubectl**
   - For Kubernetes-based deployments
   - Install from [kubernetes.io](https://kubernetes.io/docs/tasks/tools/)

## Knowledge Prerequisites

- Basic understanding of Docker concepts (containers, images, volumes)
- Familiarity with command-line operations
- Basic understanding of Python programming
- Basic knowledge of AI/ML concepts (helpful but not required)

## Workshop Materials

Please clone the following repositories before starting the workshop:

```bash
# Main workshop repository
git clone https://github.com/collabnix/genai-docker-workshop.git

# Lab 1 - Model Runner Metrics
git clone https://github.com/ajeetraina/genai-model-runner-metrics.git

# Lab 2 - Product Catalog Demo
git clone https://github.com/ajeetraina/catalog-service-demo.git
```

## Network Requirements

- Stable internet connection for downloading Docker images and dependencies
- If working in a corporate environment, ensure you have access to:
  - Docker Hub
  - GitHub
  - PyPI (Python Package Index)

## Environment Setup Verification

To verify that your environment is properly set up, run the following test container:

```bash
docker run --rm hello-world
```

If you see a "Hello from Docker!" message, your Docker installation is working correctly.

If you're ready to proceed, head over to the [Installation](installation.md) section to set up your development environment.
