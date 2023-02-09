# Docker Compose

Before docker compose we have to containerize  many microservices into different docker images and also we have to manage them individually which is not possible because a product could  contain lots of lots of microservices , and managing them could be impossible</br>
</br>
Docker compose is tool which helps in the definition of multicontainer application. Docker compose uses YAML file for every configuration and just singal command to start and stop all the services.It also provide connection  between different container of the same application </br>
</br>
It have commands to manage life cycle of docker compose application

- start, stop and rebuild services
- view the status of running services
- stream the log output of the running serivces



## Features of Docker Compose

- Have multiple isolated enviroments on a singal host
- Preserves volume when container are created
- only recreate container that have changed
- support varibale and moving a composition between enviroments


