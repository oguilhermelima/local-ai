# Local AI - CPU Models (Mac or Integrated Graphics)

This project sets up a local AI environment using Docker Compose, including Ollama for running language models and Open WebUI for a graphical interface.

## Services

The environment includes two main services:

### 1. Ollama
- Image: `ollama/ollama`
- Port: 11434
- Automatically loads the following models:
  - llama3.1
  - qwen2.5-coder
- Data is persisted in a Docker volume

### 2. Open WebUI
- Graphical interface for interacting with the models
- Port: 3000
- Accessible at: http://localhost:3000
- Automatically connects to Ollama

## How to Run

1. Make sure you have Docker and Docker Compose installed on your machine

2. Clone this repository:
```bash
git clone [REPOSITORY_URL]
cd local-ai
```

3. Start the services:
```bash
docker-compose up -d
```

4. Access the web interface at http://localhost:3000

## Useful Commands

- To stop the services:
```bash
docker-compose down
```

- To view logs:
```bash
docker-compose logs -f
```

- To restart a specific service:
```bash
docker-compose restart [service_name]
```

## Volumes

Data is persisted through two Docker volumes:
- `ollama`: Stores downloaded models
- `open-webui`: Stores web interface configurations