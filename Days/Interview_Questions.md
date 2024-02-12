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