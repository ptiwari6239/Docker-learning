# Docker Storage

## Volume 
When you create a volume, it is stored within a directory on the Docker host. When you mount the volume into a container, this directory is what is mounted into the container. This is similar to the way that bind mounts work, except that volumes are managed by Docker and are isolated from the core functionality of the host machine

1. Sharing data among multiple running containers
2. When the Docker host is not guaranteed to have a given directory or file structure. Volumes help you decouple the configuration of the Docker host from the container runtime.
3. When you want to store your container's data on a remote host or a cloud provider, rather than locally
4. When you need to back up, restore, or migrate data from one Docker host to another, volumes are a better choice.
5. When your application requires high-performance I/O on Docker Desktop


## Bind Mounts
When you use a bind mount, a file or directory on the host machine is mounted into a container. The file or directory is referenced by its full path on the host machine. The file or directory does not need to exist on the Docker host already
1. Sharing configuration files from the host machine to containers
2. Sharing source code or build artifacts between a development environment on the Docker host and a container
3. When the file or directory structure of the Docker host is guaranteed to be consistent with the bind mounts the containers require.
