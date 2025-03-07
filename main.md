## begining...

#  Essential Docker Commands for DCA Preparation  

## **1️⃣ Basic Docker Commands (Getting Started)**  
```bash
docker --version   # Check Docker version  
docker info        # Get system-wide info  
docker pull nginx  # Pull an image from Docker Hub  
docker run -d --name my_nginx -p 8080:80 nginx  # Run a container  
docker ps         # List running containers  
docker ps -a      # List all containers (including stopped ones)  
docker stop my_nginx  # Stop a container  
docker rm my_nginx    # Remove a container  
docker rmi nginx      # Remove an image  
```
## 2️⃣ Image Management

```
docker images           # List all images  
docker image inspect nginx  # Inspect image details  
docker image history nginx  # View image history (layers)  
docker tag nginx myrepo/nginx:v1  # Tag an image  
docker push myrepo/nginx:v1  # Push an image to Docker Hub  
docker pull myrepo/nginx:v1  # Pull an image from Docker Hub  
docker save -o nginx.tar nginx  # Save an image to a tar file  
docker load -i nginx.tar  # Load an image from a tar file  

```

## 3️⃣ Container Management

```
docker inspect my_container   # Get detailed container information  
docker logs my_container      # View container logs  
docker top my_container       # Show running processes inside the container  
docker exec -it my_container bash  # Access a running container shell  
docker stats my_container     # Display container resource usage statistics  
docker cp my_container:/file_path ./local_path  # Copy files from container  
docker rename my_container new_name  # Rename a container  
docker pause my_container     # Pause a running container  
docker unpause my_container   # Unpause a paused container  
docker wait my_container      # Wait until a container stops  

```

## 4️⃣ Docker Networking

```
docker network ls               # List networks  
docker network create my_network  # Create a new network  
docker network inspect my_network # View network details  
docker network connect my_network my_container  # Connect a container to a network  
docker network disconnect my_network my_container  # Disconnect a container  
docker network rm my_network  # Remove a network  
```

## 5️⃣ Docker Volumes & Storage

```
docker volume ls         # List all volumes  
docker volume create my_volume  # Create a new volume  
docker volume inspect my_volume # View volume details  
docker volume rm my_volume  # Remove a volume  
docker run -d -v my_volume:/app/data --name my_app nginx  # Run a container with a volume  
docker run -d --mount type=bind,source="$(pwd)"/data,target=/app/data nginx  # Use bind mount  
```
## 6️⃣ Docker Compose (Multi-container Apps)

```
docker-compose up -d       # Start all services in the background  
docker-compose down        # Stop and remove containers, networks, volumes  
docker-compose logs -f     # View real-time logs of services  
docker-compose ps          # List running services  
docker-compose restart my_service  # Restart a service  
```

## 7️⃣ Docker Swarm (Orchestration)

```
docker swarm init                 # Initialize Docker Swarm mode  
docker node ls                     # List nodes in the Swarm  
docker service create --name my_service -p 8080:80 nginx  # Create a service  
docker service ls                   # List all services  
docker service scale my_service=3    # Scale a service to 3 replicas  
docker service update --image nginx:latest my_service  # Update a service  
docker stack deploy -c docker-compose.yml my_stack  # Deploy a stack  
docker stack rm my_stack            # Remove a stack  
```
## 8️⃣ Docker Security & User Management

```
docker login                        # Login to Docker Hub  
docker logout                       # Logout from Docker Hub  
docker secret create my_secret file.txt  # Create a secret  
docker secret ls                    # List secrets  
docker secret inspect my_secret      # Inspect a secret  
docker secret rm my_secret           # Remove a secret  
```

## 9️⃣ Docker System & Troubleshooting

```
docker system df       # Show Docker disk usage  
docker system prune    # Remove unused data (containers, images, networks)  
docker events         # Show real-time events from the Docker daemon  
docker info           # Get detailed system-wide information  
docker version        # Show Docker client and server versions  
```


