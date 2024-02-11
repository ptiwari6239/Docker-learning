# Interview Question On Docker !!


## BASIC QUESTION !!    
### Docker is very popular and powerfull open source containerization platform that is used for building, deploying and running application . 

## what is virtualization ?
**virtualization is the creation of virtual --rather than actual-- version of something, such as an operating system, a server, a storage device or network resource.It allow organization to operate multiple system and application on a single server**

### What is hypervisor ?
**A hypervisor is a software that makes virtualization possible.It divides the host system and allocates the resources to each divided virtual environment**

### What is containerization ?
**Usually, in the software development process, code developed on one machine might not work perfectly fine on any other machine because of the dependencies. This problem was solved by the containerization concept. So basically, an application that is being developed and deployed is bundled and wrapped together with all its configuration files and dependencies. This bundle is called a container. Now when you wish to run the application on another system, the container is deployed which will give a bug-free environment as all the dependencies and libraries are wrapped together. Most famous containerization environments are Docker and Kubernetes.**

### Difference between virtualization and containerization 

**Containers provide an isolated environment for running the application. The entire user space is explicitly dedicated to the application. Any changes made inside the container is never reflected on the host or even other containers running on the same host. Containers are an abstraction of the application layer. Each container is a different application.</br></br>Whereas in Virtualization, hypervisors provide an entire virtual machine to the guest(including Kernal). Virtual machines are an abstraction of the hardware layer. Each VM is a physical machine. VM is more isolated and heavy and takes a lot time to start.**


### What is docker image ?
**Docker image is the source of Docker container. In other words, Docker images are used to create containers. When a user runs a Docker image, an instance of a container is created. These docker images can be deployed to any Docker environment.**

### Docker Architecture
[Answer](https://github.com/ptiwari6239/Docker-learning/blob/master/Days/Docker-architecture.md)
### What is docker file
**Docker can build images automatically by reading the instructions from a file called Dockerfile.</br>A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.**
