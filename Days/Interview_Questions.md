# Interview Question On Docker !!


## BASIC QUESTION !!    
---
### Docker is very popular and powerfull open source containerization platform that is used for building, deploying and running application . 

### what is virtualization ?
**virtualization is the creation of virtual --rather than actual-- version of something, such as an operating system, a server, a storage device or network resource.It allow organization to operate multiple system and application on a single server**

### What is hypervisor ?
**A hypervisor is a software that makes virtualization possible.It divides the host system and allocates the resources to each divided virtual environment**

### What is containerization ?
**Usually, in the software development process, code developed on one machine might not work perfectly fine on any other machine because of the dependencies. This problem was solved by the containerization concept. So basically, an application that is being developed and deployed is bundled and wrapped together with all its configuration files and dependencies. This bundle is called a container. Now when you wish to run the application on another system, the container is deployed which will give a bug-free environment as all the dependencies and libraries are wrapped together. Most famous containerization environments are Docker and Kubernetes.**

### Difference between virtualization and containerization 

**Containers provide an isolated environment for running the application. The entire user space is explicitly dedicated to the application. Any changes made inside the container is never reflected on the host or even other containers running on the same host. Containers are an abstraction of the application layer. Each container is a different application.</br></br>Whereas in Virtualization, hypervisors provide an entire virtual machine to the guest(including Kernal). Virtual machines are an abstraction of the hardware layer. Each VM is a physical machine. VM is more isolated and heavy and takes a lot time to start.**


### What is docker image ?
**Docker image is the source of Docker container. In other words, Docker images are used to create containers. When a user runs a Docker image, an instance of a container is created. These docker images can be deployed to any Docker environment.**


### What is container ?
**Containers are a type of software that can virtually package and isolate applications for deployment. Containers package an application's code and dependencies together, letting the application reliably run in all computing environments.<br>Containers share access to an operating system (OS) kernel without the traditional need for virtual machines (VMs). Containers can be used to run small microservices, larger applications or even lightweight container OSes.**

### Benefits of containers ?
- Light Weight
- portable and platform-independent
- Improves utilization
- Supports modern development and architecture
  
### Use cases of Containers ?

- microservices
- DevOps
- Hybrid,multicloud
- Application modernizing and  migration.
  
  


### Docker Architecture
[Answer](https://github.com/ptiwari6239/Docker-learning/blob/master/Days/Docker-architecture.md)



### What is docker Swarm ?
**Docker Swarm is an orchestration management tool that runs on Docker applications. It helps end-users in creating and deploying a cluster of Docker nodes.**



### What is docker file

**Docker can build images automatically by reading the instructions from a file called Dockerfile.</br>A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.**



### What if Docker image 
[Answer](https://github.com/ptiwari6239/Docker-learning/blob/master/Days/Day02/Important_Terminologies_in_Docker.md)


### What is Docker Compose ?

**Docker Compose is a YAML file which contains details about the services, networks, and volumes for setting up the Docker application. So, you can use Docker Compose to create separate containers, host them and get them to communicate with each other. Each container will expose a port for communicating with other containers.**

### What is docker namespace ?
**In Docker, namespaces are a key feature used to provide process isolation within containers. Docker utilizes Linux namespaces to create an isolated environment for each container, allowing processes within the container to have their own view of system resources, distinct from processes outside the container.**

### Docker container/image lifecycle 

- Create container
- Run docker container
- Pause container
- Unpause container
- Start container
- Stop container
- Restart container
- Kill container
- Destroy container

  
### Describe the process of process of containerizating an application 
- write a dockerfile/containerfile that includes your app and its dependencies and command.
- build the image using same file
- push the image to remote repository (optional)
- run the container using the same image.

## IMAGES
---
### why are container images so small ?
- most of the container images don't need kernal. they share and access of the host system
- Containers intended to run specific application in most cases. This means they hold only what the application needs in order to run

### Explain container image layers
- The layers of an image is where all the content is stored - code, files, etc.
- Each layer is independent
- Each layer has an ID that is an hash based on its content
- The layers (as the image) are immutable which means a change to one of the layers can be easily identified

## Containerfile/Dockerfile
---
### What is containerfile/dockerfile
**A dockerfile/containerfile is text file that contains all the instruction for building an image which containers can use.**

### List five different instructions that are available for use in a Containerfile/Dockerfile
- WORKDIR: sets the working directory inside the image filesystems for all the instructions following it
- EXPOSE: exposes the specified port (it doesn't adds a new layer, rather documented as image metadata)
- ENTRYPOINT: specifies the startup commands to run when a container is started from the image
- ENV: sets an environment variable to the given value
- USER: sets the user (and optionally the user group) to use while running the image

### What is the difference between ADD and COPY in Containerfile/Dockerfile?
**COPY takes in a source and destination. It lets you copy in a file or directory from the build context into the Docker image itself.ADD lets you do the same, but it also supports two other sources. You can use a URL instead of a file or directory from the build context. In addition, you can extract a tar file from the source directly into the destination.**

### Q.What is the difference between CMD and RUN in Containerfile/Dockerfile?
**RUN lets you execute commands inside of your Docker image. These commands get executed once at build time and get written into your Docker image as a new layer. CMD is the command the container executes by default when you launch the built image. A Containerfile/Dockerfile can only have one CMD. You could say that CMD is a Docker run-time operation, meaning it’s not something that gets executed at build time. It happens when you run an image. A running image is called a container.**


## STORAGE 

---
### Q. Container storage is said to be ephemeral ? What does it mean
**Data generated by container will get deleted once container is removed**
###

## Architecuter
---
### Q. how container achieve isolation from the rest of the system?
**Docker uses linux feature called namespace and cgroup to isolate each container**

### Describe difference between cgroup and namespace 
**Control Groups: provide a mechanism for aggregating/partitioning sets of tasks, and all their future children, into hierarchical groups with specialized behavior**</br>
**namespace: wraps a global system resource in an abstraction that makes it appear to the processes within the namespace that they have their own isolated instance of the global resource.**

### what components are part of docker engine ?
- docker engine 
- containerd
- runc
### Explain image layers ?
**A Docker image is composed of multiple layers stacked on top of each other. Each layer represents a specific modification to the file system (inside the container), such as adding a new file or modifying an existing one**

### what does .dockerignore used for ?
**By default, Docker uses everything (all the files and directories) in the directory you use as build context. .dockerignore used for excluding files and directories from the build context**


###