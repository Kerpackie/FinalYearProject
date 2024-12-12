
1. **List all Docker containers**:
    ```sh
    docker ps
    ```
    - Use `docker ps -a` to list all containers, including stopped ones.

2. **Start a Docker container**:
    ```sh
    docker start <container_id>
    ```

3. **Stop a Docker container**:
    ```sh
    docker stop <container_id>
    ```

4. **Remove a Docker container**:
    ```sh
    docker rm <container_id>
    ```

5. **List all Docker images**:
    ```sh
    docker images
    ```

6. **Pull a Docker image from a repository**:
    ```sh
    docker pull <image_name>
    ```

7. **Run a Docker container from an image**:
    ```sh
    docker run -d -p <host_port>:<container_port> <image_name>
    ```
    - Use `-d` to run the container in detached mode.
    - Use `-p` to map ports.

8. **Build a Docker image from a Dockerfile**:
    ```sh
    docker build -t <image_name> <path_to_dockerfile>
    ```

9. **Tag a Docker image**:
    ```sh
    docker tag <image_id> <repository_name>:<tag>
    ```

10. **Push a Docker image to a repository**:
    ```sh
    docker push <repository_name>:<tag>
    ```

11. **Remove a Docker image**:
    ```sh
    docker rmi <image_id>
    ```

12. **View logs of a Docker container**:
    ```sh
    docker logs <container_id>
    ```

13. **Execute a command in a running Docker container**:
    ```sh
    docker exec -it <container_id> <command>
    ```
    - Use `-it` to run in interactive mode.

14. **Inspect a Docker container**:
    ```sh
    docker inspect <container_id>
    ```

15. **Prune unused Docker objects**:
    ```sh
    docker system prune
    ```
    - This command removes all stopped containers, unused networks, and dangling images.

These commands will help you manage Docker containers and images effectively.