## Basic Commands Of Docker</br>

1. It tell version of docker version installed
``docker --version``</br>
![docker_version](/images/docker_version_ss.png)
</br>

2. It tell all the running containers``docker ps``</br>
![docker_ps](/images/docker_ps_ss.png)
</br>

3. It tell all the container running and stop ``docker ps -a``
![docker_allProcess](/images/docker_allProcess_ss.png)
</br>

4. Shows all the images ``docker images``
![docker_images](/images/docker_images.png)
</br>

5. Pulls images from docker hub ``docker pull <iamges_name>``
![docker_pull](/images/docker_pull_ss.png)
</br>

6. Run an instance of docker images . ``docker run <image_name>`` this also pull and run an image if not in local host.
![docker_run](/images/docker_run_ss.png)

</br>

7. Stop the running container ``docker stop <container_id>``</br>
![docker_stop](/images/docker_stop_ss.png)

</br>

8. Remove  the container from local host ``docker rm <container_id>``</br>
</br>


9.Remove the images from local host ``docke rmi <image_id>``</br>
![docker_rmi](/images/docker_rmi_ss.png)

</br>


10. This command is used to access the running container `` docker exec -it <container_id> /bin/bash``</br>



