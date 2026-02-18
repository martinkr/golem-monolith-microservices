# Monolith to Microservices — Evolution example

This repository demonstrates the progression from a monolithic architecture to a fully distributed microservices system. Each folder represents a different architectural stage:

## Folder Overview

- **`01_monolith/`** — Single monolithic application with all logic in one file
- **`02_modulith/`** — Modular monolith: still a single process, but organized into logical service modules
- **`03_microservices/`** — Fully distributed microservices: independent services, separate processes
- **`microservices/`** — Additional microservices examples or helper modules

## Architecture Stages

### Stage 1: Monolith (`01_monolith/`)

Single file, single process. Everything together.

```bash
cd 01_monolith
node index.js
```

### Stage 2: Modulith (`02_modulith/`)

Still a single process and entry point, but code is organized into separate logical modules (services):
- `data-service.js`
- `aggregation-service.js`

```bash
cd 02_modulith
node index.js
```

### Stage 3: Microservices (`03_microservices/`)

Each service runs in its own process. Services communicate over the network (HTTP, etc.).

```bash
cd 03_microservices
npm install
npm run start
```

## Quick Start — Run the final microservices setup

From the root of this repository:

```bash
cd 03_microservices
npm install
npm run start
```

This starts the full microservices demo (usually on `http://localhost:3000` or similar). Check the server output for the exact URL.

## Prerequisites

- Node.js  
- npm

## Learning Notes

- Review each stage in order to understand the architectural evolution
- `01_monolith/` shows the original single-file design
- `02_modulith/` shows internal organization without distributed architecture
- `03_microservices/` shows how to split into separate processes and services
- Each stage uses plain JavaScript with minimal dependencies (Express, axios, etc.)

## Additional Resources

- Review `package.json` in each folder for dependencies and scripts
- Check `serve.js` in `03_microservices/` for the orchestration logic
- Inspect `services/` folders to see service implementations

 
