# Docker Commands 

1. **`docker --version`**  
   Displays the current version of Docker installed on your machine.

2. **`docker ps`**  
   Lists all running Docker containers.

3. **`docker ps -a`**  
   Lists all containers, including the stopped ones.

4. **`docker run <image>`**  
   Runs a container from the specified image.

5. **`docker run -it <image>`**  
   Runs a container interactively with a terminal session.

6. **`docker run -d <image>`**  
   Runs a container in detached mode (in the background).

7. **`docker exec -it <container_id> bash`**  
   Opens an interactive bash shell inside a running container.

8. **`docker stop <container_id>`**  
   Stops a running container.

9. **`docker start <container_id>`**  
   Starts a stopped container.

10. **`docker restart <container_id>`**  
    Restarts a running or stopped container.

11. **`docker kill <container_id>`**  
    Immediately stops a container by sending a SIGKILL signal.

12. **`docker rm <container_id>`**  
    Removes a container from the system (requires the container to be stopped).

13. **`docker rmi <image_id>`**  
    Removes an image from the system.

14. **`docker images`**  
    Lists all Docker images available locally.

15. **`docker build -t <image_name>:<tag> <path>`**  
    Builds an image from a Dockerfile at the specified path.

16. **`docker pull <image>`**  
    Downloads a Docker image from a registry (e.g., Docker Hub).

17. **`docker push <image>`**  
    Uploads a Docker image to a registry.

18. **`docker logs <container_id>`**  
    Displays the logs of a running or stopped container.

19. **`docker inspect <container_id>`**  
    Provides detailed information about a container or image in JSON format.

20. **`docker network ls`**  
    Lists all Docker networks.

21. **`docker network create <network_name>`**  
    Creates a new Docker network.

22. **`docker network inspect <network_name>`**  
    Displays detailed information about a specific Docker network.

23. **`docker volume ls`**  
    Lists all Docker volumes.

24. **`docker volume create <volume_name>`**  
    Creates a new Docker volume.

25. **`docker volume inspect <volume_name>`**  
    Displays detailed information about a specific Docker volume.

26. **`docker-compose up`**  
    Starts and runs containers defined in a docker-compose.yml file.

27. **`docker-compose up -d`**  
    Starts and runs containers in detached mode, defined in a docker-compose.yml file.

28. **`docker-compose down`**  
    Stops and removes containers, networks, and volumes created by `docker-compose up`.

29. **`docker-compose logs`**  
    Shows logs for services defined in the docker-compose.yml file.

30. **`docker-compose exec <service_name> bash`**  
    Opens a shell in a running service container.

31. **`docker stats`**  
    Displays real-time statistics for all running containers.

32. **`docker system prune`**  
    Removes unused Docker data (e.g., stopped containers, unused images, and networks).

33. **`docker system df`**  
    Displays disk space usage for Docker images, containers, and volumes.

34. **`docker login <registry>`**  
    Logs into a Docker registry (e.g., Docker Hub).

35. **`docker logout <registry>`**  
    Logs out of a Docker registry.

36. **`docker update <container_id>`**  
    Updates the configuration of a running container (e.g., resource limits).

37. **`docker exec -it <container_id> sh`**  
    Opens a shell inside a running container if bash is unavailable.

38. **`docker pull <image>:<tag>`**  
    Pulls a specific version (tag) of an image from a Docker registry.

39. **`docker tag <image_id> <new_image_name>:<new_tag>`**  
    Tags an image with a new name or version.

40. **`docker volume rm <volume_name>`**  
    Removes a Docker volume.

41. **`docker run --rm <image>`**  
    Runs a container and removes it automatically when it stops.

42. **`docker build --no-cache -t <image_name> .`**  
    Builds a Docker image without using the cache from previous builds.

43. **`docker exec -u <user_id>:<group_id> <container_id> <command>`**  
    Executes a command as a specific user inside a container.

44. **`docker cp <container_id>:<path_in_container> <host_path>`**  
    Copies files or directories from a container to the host machine.

45. **`docker cp <host_path> <container_id>:<path_in_container>`**  
    Copies files or directories from the host machine to a container.

46. **`docker commit <container_id> <new_image_name>`**  
    Creates a new image from the current state of a container.

47. **`docker push <registry>/<image_name>:<tag>`**  
    Pushes a Docker image to a remote registry (e.g., Docker Hub).

48. **`docker history <image_name>`**  
    Displays the history of an image, including all layers.

49. **`docker attach <container_id>`**  
    Attaches to a running container's main process and provides interactive access.

50. **`docker exec <container_id> <command>`**  
    Executes a command in a running container.
    
*Additional Commands:*

51. **`docker-compose build`**  
    Builds images for services defined in a docker-compose.yml file.

52. **`docker-compose stop`**  
    Stops services defined in a docker-compose.yml file without removing them.

53. **`docker-compose restart`**  
    Restarts services defined in a docker-compose.yml file.

54. **`docker-compose run <service_name> <command>`**  
    Runs a one-off command in a new container for the specified service.

55. **`docker-compose exec <service_name> <command>`**  
    Executes a command inside a running container of the specified service.

56. **`docker-compose ps`**  
    Lists all the containers related to the services defined in a docker-compose.yml file.

57. **`docker-compose config`**  
    Validates and displays the configuration of a docker-compose.yml file.

58. **`docker build -t <image_name> --build-arg <arg_name>=<value> .`**  
    Builds a Docker image, passing build-time variables to the Dockerfile.

59. **`docker network create --driver <network_driver> <network_name>`**  
    Creates a Docker network with a specified driver (e.g., bridge, overlay).

60. **`docker network connect <network_name> <container_id>`**  
    Connects a running container to a Docker network.

61. **`docker network disconnect <network_name> <container_id>`**  
    Disconnects a running container from a Docker network.

62. **`docker run --name <container_name> <image>`**  
    Runs a container with a specific name.

63. **`docker run -v <host_path>:<container_path>`**  
    Mounts a volume or directory from the host into a container.

64. **`docker run --memory <memory_limit> <image>`**  
    Limits the memory available to a container.

65. **`docker run --cpu-shares <cpu_shares> <image>`**  
    Specifies the CPU shares (relative weight) for the container.

66. **`docker run --cpus <cpu_limit> <image>`**  
    Limits the number of CPUs available to a container.

67. **`docker run --network <network_name> <image>`**  
    Specifies the network the container should connect to.

68. **`docker volume prune`**  
    Removes all unused Docker volumes.

69. **`docker network prune`**  
    Removes all unused Docker networks.

70. **`docker system prune --volumes`**  
    Removes unused containers, networks, images, and volumes.

71. **`docker build -t <image_name> --no-cache .`**  
    Builds a Docker image without using any cached layers.

72. **`docker inspect --format '{{.NetworkSettings.IPAddress}}' <container_id>`**  
    Displays the IP address of a container using Go templating.

73. **`docker stats <container_id>`**  
    Shows real-time resource usage (CPU, memory, I/O, etc.) for a container.

74. **`docker update --memory <memory_limit> --cpus <cpu_limit> <container_id>`**  
    Updates the memory and CPU limits of a running container.

75. **`docker run --entrypoint <command> <image>`**  
    Overrides the default entry point of an image.

76. **`docker exec <container_id> <command>`**  
    Executes a command inside a running container.

77. **`docker volume create --driver <driver_name> <volume_name>`**  
    Creates a volume with a specific driver.

78. **`docker-compose scale <service_name>=<number_of_instances>`**  
    Scales the number of container instances for a specified service in docker-compose.yml.

79. **`docker-compose logs -f <service_name>`**  
    Follows the logs of a specific service defined in docker-compose.yml.

80. **`docker cp <container_id>:<path_in_container> <host_path>`**  
    Copies files or directories from a container to the host machine.

81. **`docker cp <host_path> <container_id>:<path_in_container>`**  
    Copies files or directories from the host to a container.

82. **`docker exec <container_id> cat <file_path>`**  
    Runs the cat command to display the contents of a file inside a container.

83. **`docker exec <container_id> tail -f <log_file>`**  
    Monitors the log file inside a running container in real-time.

84. **`docker save -o <output_file.tar> <image_name>`**  
    Saves a Docker image to a tarball file.

85. **`docker load -i <input_file.tar>`**  
    Loads a Docker image from a tarball file.

86. **`docker info`**  
    Displays detailed information about the Docker installation (e.g., version, number of containers, and images).

87. **`docker events`**  
    Displays a stream of Docker events in real-time (e.g., container creation, image pull).

88. **`docker volume inspect <volume_name>`**  
    Displays detailed information about a Docker volume.

89. **`docker network inspect <network_name>`**  
    Displays detailed information about a Docker network.

90. **`docker build --file <dockerfile_path> .`**  
    Specifies the Dockerfile path when building an image.

91. **`docker run -p <host_port>:<container_port> <image>`**  
    Maps a container's port to a host's port.

92. **`docker run --link <container_name>:<alias> <image>`**  
    Links two containers together, allowing them to communicate by alias.

93. **`docker run --env <env_variable>=<value> <image>`**  
    Sets an environment variable inside the container.

94. **`docker exec -u root <container_id> <command>`**  
    Executes a command as the root user inside the container.

95. **`docker pull --all-tags <image>`**  
    Pulls all tags of a Docker image from a registry.

96. **`docker push <username>/<image_name>:<tag>`**  
    Pushes a Docker image with a specified tag to a Docker registry.

97. **`docker tag <image_id> <username>/<image_name>:<tag>`**  
    Tags a local image for easier reference before pushing to a registry.

98. **`docker history <image_name>`**  
    Shows the history of an image, including all layers.

99. **`docker inspect <container_id>`**  
    Provides detailed information about a container in JSON format.

100. **`docker exec <container_id> <command>`**  
    Executes a command in a running container.

