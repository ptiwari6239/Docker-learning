# Dockerfile commands


1. ``FROM`` this statement defines which image to download and start from. it must be first command in dockerfile to be called a valid file . A dockerfile can have multiple ``FROM`` command within a single file to create multiple images or use one build stage as a dependency for another.</br>


</br>

2. ``RUN`` The RUN statement defines running a command through the shell, waiting for it to finish, and saving the result. It tells what process will be running inside the container at the run time.

</br>

3. ``ADD`` Give instruction to copy new files, directories  and add them to the filesystem of the image.
</br>

4. ``ENV`` this statement sets the enviroment variables both during the build and when running the result.
</br>


5. ``ENTRYPOINT`` it specifies the start of the command to run. If container acts as a command-line program, it can use  ENTRYPOINT.
</br>

6. ``CMD`` this  command is use  to launch the software required in a container. It specifies the whole command to run .


7. ``WORKDIR`` it sets the directory that the container starts in .
