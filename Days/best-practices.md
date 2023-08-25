# Docker Best Practices

1. Use official Docker images as base images instead of base operating system images

2. User specific image version , do not use a random latest tag fixate the version 

3. User smaller-sized official images, use image based on a leaner and smaller and distro

4. Optimize caching images layers, order dockerfile commands froml least to most frequently changing

5. Use .dockerignore to explicitly exclude files and folders

6. Make use of "multi-stage builds"

7. Use the least privileged user

8. Scan images for vulnerabilites


