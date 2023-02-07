# Docker Networking 

- Docker networking enables us to link a docker container to as many networks as requires.
- Docker networking provides us a complete isolation to docker container.</br>

**Note** We can add containers to more than one network .</br>

## How it works
</br>

![Docker-image-container](/images/docker-image-life-cycle.png)

- Docker file creates a docker image using build command
- Docker image container all the project's code and dependices
- using docker image, we can run the code in order to create the docker container.
</br>

## Advantages of Docker Networking

- rapid develoyment 
- portability 
- better efficiency
- faster configurating 
- scalability 
- security
---


# Network Drivers in Docker 

## Bridge
- It is a private default network created on the host.
- Containers linked to this network  have an internal ip address through which they communicate with each other easily
- The Docker server(daemon) creates virtual ethernet bridge **docker0** that performs the operating by automatically delivering packets among various network interfaces.
- These are widely used when applications are executed in a standalone container

## Host
- It is a public network 
- It utilize the host's ip address and TCP port space in order to display the server running inside the container
- It effectively disables network isolation between the docker host and docker container which menas using this network driver a use will be unable to run mutliple container on the same host.

## None
-  In this network driver, the docker container will neither have access to external network nor will it be able to communicate with other container.
- this option is used when a user wants to disable the networking access to a container.
- in simple terms, None is called loopback interface which means it has no external network interface.

## Overlay

- this is utilized for creating an internal private network to the docker nodes in the docker swarm cluster.

## Macvlan

-  it simplifies the communcation process between containers.

- this network assigns a MAC address to the docker continer. with this MAC address, the docker server (daemon) routes the network traffic to a router.
- it is suitable when a user wants to directly connect the container to the physical network rather than Docker host's