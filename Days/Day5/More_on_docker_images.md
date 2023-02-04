
# Dockerfile Syntax

**To create our own docker image from application code**

After creating an application we need to deploy it , to do this, it must be packaged to its own docker container . It means we need to build an docker image for our application .

***
### Syntax for Dockerfile

```bash
FROM <image> (*)
ENV <>
RUN <commmand> # to execute any linux command inside the container 
COPY <source> <destination>
CMD (*) 
```
After creating an Dockerfile , run this command to build an image out of it .
```bash
docker build -t <image_name>:<version> <path to dockerfile>
```
To check if image is created or not 
```bash
docker images
````
----
