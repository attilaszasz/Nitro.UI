# Nitro.UI
A lightweight UI for Nitro, dockerized for easy deloyment

Please check out the [Nitro](https://nitro.jan.ai/docs) documentation for more information and usage.

## Getting Started

### Prerequisites
- [Docker](https://docs.docker.com/get-docker/)

### Installation

```bash
docker run -d --name nitro -p 3928:3928 -v ./models:/models ghcr.io/attilaszasz/nitro:latest
```

Alternatively, you can use the `docker-compose.yml` file in this repository.

The './models' directory is where you can store your models.

## Web UI
Coming soon...