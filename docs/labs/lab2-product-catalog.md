# Lab 2: Product Catalog Demo

In this lab, we'll implement a practical GenAI application: a product catalog service enhanced with AI capabilities. We'll use the [catalog-service-demo](https://github.com/ajeetraina/catalog-service-demo) project to build, deploy, and interact with this application.

## Objectives

By the end of this lab, you will be able to:

1. Deploy a microservices architecture with GenAI components
2. Integrate a language model into a product catalog application
3. Use Docker to manage the complete application stack
4. Test AI-enhanced product search and recommendations
5. Understand the patterns for integrating GenAI into business applications

## Prerequisites

Ensure you have the following set up:

- Docker Desktop installed and running
- Git installed
- At least 8GB of RAM available
- Basic knowledge of Docker, Docker Compose, and REST APIs
- The lab repository cloned:
  ```bash
  git clone https://github.com/ajeetraina/catalog-service-demo.git
  cd catalog-service-demo
  ```

## Lab Instructions

Detailed instructions for this lab can be found in the [catalog-service-demo repository](https://github.com/ajeetraina/catalog-service-demo).

### Key Steps

1. Clone the lab repository
2. Build and start the application using Docker Compose
3. Explore the product catalog through the web interface
4. Test the AI-enhanced search capabilities
5. Examine the recommendation engine
6. Analyze the microservices architecture

## Application Architecture

The application consists of several microservices:

- **Catalog Service**: Core service managing product data
- **Search Service**: AI-enhanced search functionality
- **Recommendation Engine**: AI-powered product recommendations
- **Frontend**: Web interface for interacting with the catalog
- **Database**: Storage for product data
- **Vector Store**: For semantic search capabilities
- **Model Service**: Containerized language model for AI features

## Resources

- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Microservices Architecture Patterns](https://microservices.io/patterns/index.html)
- [Vector Database Concepts](https://www.pinecone.io/learn/vector-database/)

## Next Steps

After completing this lab, explore the [Resources](../resources/links.md) section for additional learning materials and community resources.
