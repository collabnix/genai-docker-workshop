# Frequently Asked Questions

This page addresses common questions about GenAI with Docker, the workshop, and related technologies.

## General Questions

### What is GenAI?

Generative AI (GenAI) refers to artificial intelligence systems that can create new content, including text, images, audio, and more. These systems are trained on vast amounts of data and learn patterns that allow them to generate outputs resembling human-created content.

### Why use Docker for GenAI applications?

Docker provides several benefits for GenAI applications:
- **Consistency**: Ensuring models run the same way across all environments
- **Dependency Management**: Packaging all dependencies together
- **Resource Isolation**: Allocating appropriate resources to each model
- **Scalability**: Easily scaling instances based on demand
- **Reproducibility**: Creating reproducible environments for development and production

### Do I need a GPU to run GenAI models with Docker?

While many GenAI models benefit significantly from GPU acceleration, it's not always required:
- **Development & Testing**: You can develop and test with CPU-only configurations
- **Small Models**: Smaller, optimized models can run reasonably well on CPUs
- **Quantized Models**: INT8 or FP16 quantized models require less computational power
- **Cloud GPUs**: You can use cloud-based GPU resources for production deployment

## Workshop-Specific Questions

### What knowledge do I need before taking this workshop?

This workshop assumes:
- Basic understanding of Docker concepts (containers, images, volumes)
- Familiarity with command-line operations
- Basic understanding of Python programming
- Basic knowledge of AI/ML concepts (helpful but not required)

### Can I run the workshop labs on my laptop?

Yes, most labs are designed to run on a standard laptop with:
- 4+ CPU cores
- 8GB+ RAM (16GB recommended)
- Docker Desktop installed
- Internet connection for pulling images

Some advanced exercises may benefit from a GPU, but alternatives are provided.

### Will I be able to deploy my own models after this workshop?

Yes! By the end of this workshop, you'll have the knowledge to:
- Package your own GenAI models in Docker containers
- Deploy models using Docker's Model Runner
- Set up monitoring and scaling for your models
- Follow best practices for production deployment

## Technical Questions

### How do I handle large model weights with Docker?

Large model weights can be managed in several ways:
- **Volume Mounting**: Keep model weights in volumes rather than in images
- **Multi-stage Builds**: Download weights during container build
- **Registry Extensions**: Use Docker Hub or other registries designed for ML artifacts
- **External Storage**: Use object storage like S3 and download at runtime

### What's the difference between Model Runner and MCP Toolkit?

- **Model Runner**: Focused on efficiently running and serving AI models with optimized performance
- **MCP Toolkit**: A broader suite of tools for managing the entire lifecycle of containerized models, including deployment, monitoring, and scaling

### How do I scale GenAI models for production traffic?

Several strategies can be used:
- **Horizontal Scaling**: Deploy multiple container instances behind a load balancer
- **Auto-scaling**: Use orchestration platforms to scale based on metrics
- **Batching**: Implement request batching for better throughput
- **Load Balancing**: Distribute requests across multiple instances
- **Caching**: Implement response caching for common requests

### Can I deploy quantized models with Docker?

Yes! Docker works well with quantized models:
- **Format Support**: Model Runner supports common quantized formats (INT8, FP16)
- **Performance Benefits**: Quantized models require less memory and compute
- **Deployment Options**: Various inference servers that support quantization can be containerized

## Docker-Specific Questions

### Do I need Docker Desktop or can I use Docker Engine?

Either works fine for this workshop:
- **Docker Desktop**: Recommended for Windows and Mac users for ease of use
- **Docker Engine**: Suitable for Linux users or server deployments

### How do I enable GPU support in Docker?

To enable GPU support:
1. Install the NVIDIA driver for your GPU
2. Install the [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-container-toolkit)
3. Restart the Docker daemon
4. Use the `--gpus` flag when running containers: `docker run --gpus all ...`

### Can I use Docker Compose with GenAI applications?

Absolutely! Docker Compose is excellent for:
- **Development Environments**: Setting up complete development stacks
- **Multi-container Applications**: Coordinating model servers with databases and APIs
- **Resource Configuration**: Declaring GPU and memory requirements
- **Network Configuration**: Setting up communication between services

## Contributing and Support

### How can I contribute to this workshop?

You can contribute in several ways:
- **Submit Issues**: Report bugs or suggest improvements on GitHub
- **Pull Requests**: Contribute code, documentation, or new labs
- **Share Knowledge**: Help others in the community forums
- **Spread the Word**: Share the workshop with colleagues and on social media

### Where can I get help if I'm stuck?

If you need assistance:
- **GitHub Issues**: [File an issue](https://github.com/collabnix/genai-docker-workshop/issues/new)
- **Slack Community**: Join the [Collabnix Slack](https://launchpass.com/collabnix)
- **Discussion Forums**: Participate in workshop discussions
- **Community Resources**: Check the [Useful Links](links.md) section

### Will this workshop be updated regularly?

Yes! The GenAI and Docker landscapes evolve rapidly, and we're committed to keeping this workshop current with:
- New Docker features for AI workloads
- Emerging GenAI techniques and models
- Updated deployment patterns and best practices
- Additional labs and examples

Keep an eye on the repository for updates, or star it to receive notifications.
