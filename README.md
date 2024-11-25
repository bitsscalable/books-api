
## Prerequisites

Ensure you have the following installed on your system:

- [Docker](https://www.docker.com/) (for containerization)

- Create a local docker network

```
docker network create mynetwork

```

- Run the mongodb as a container
```
docker run --name mongo-db  --network mynetwork  -p 27017:27017 -d mongo:latest
```

## Getting Started

### Step 1: Clone the Repository

```bash
git clone https://github.com/bitsscalable/books-api.git
cd books-api
```

### Step 2: Build the Docker image

docker build -t books-api .

### Step 3: Run the container

docker run --name books-api --network mynetwork -d -p 8081:8081 books-api



