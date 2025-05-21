# Lab 1: Model Runner Metrics

In this lab, we'll explore how to use Docker's Model Runner to deploy a generative AI model and collect performance metrics. We'll use the [genai-model-runner-metrics](https://github.com/ajeetraina/genai-model-runner-metrics) project to visualize and analyze these metrics.

## Objectives

By the end of this lab, you will be able to:

1. Deploy a language model using Docker's Model Runner
2. Configure and collect performance metrics
3. Visualize metrics using Prometheus and Grafana
4. Analyze performance under different load conditions
5. Optimize model configuration based on metrics

## Prerequisites

Ensure you have the following set up:

- Docker Desktop installed and running
- Git installed
- At least 8GB of RAM available
- Approximately 20GB of free disk space
- Basic knowledge of Docker and Docker Compose
- The lab repository cloned:
  ```bash
  git clone https://github.com/ajeetraina/genai-model-runner-metrics.git
  cd genai-model-runner-metrics
  ```

## Lab Instructions

Detailed instructions for this lab can be found in the [genai-model-runner-metrics repository](https://github.com/ajeetraina/genai-model-runner-metrics).

### Key Steps

1. Clone the lab repository
2. Start the services using Docker Compose
3. Access the model through the provided API
4. Explore metrics in Prometheus and Grafana
5. Run load tests to analyze performance
6. Optimize model configuration

## Resources

- [Model Runner Documentation](https://docs.docker.com/genai/model-runner/)
- [Prometheus Documentation](https://prometheus.io/docs/introduction/overview/)
- [Grafana Documentation](https://grafana.com/docs/grafana/latest/)

## Next Steps

After completing this lab, proceed to [Lab 2: Product Catalog Demo](lab2-product-catalog.md) to explore a more complex GenAI application.
