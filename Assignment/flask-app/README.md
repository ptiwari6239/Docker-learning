# Dockerfile for the flask-app

**STEPS**

1. create an directory named flask-app
2. copy every files and code present in this directory
3. make sure to change directory ``cd flask-app`` 
4. now create a file named ``Dockerfile`` with following content 
```bash
# base image
FROM alpine:3.5
# install python and pip  
RUN apk add --update py2-pip
# copy and install python module
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt
# copy required file 
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/
# tell the port number the container should expose
EXPOSE 5000
# run the application 
CMD ["python","/usr/src/app/app.py"]

```
5. now build the image from ``Dockerfile`` using the command
```bash
root@ubuntu:/home/ptiwari/gitrepo/Docker-learning/Assignment/flask-app# docker build -t myfirstapp:1.01 .
Sending build context to Docker daemon   7.68kB
Step 1/8 : FROM alpine:3.5
 ---> f80194ae2e0c
Step 2/8 : RUN apk add --update py2-pip
 ---> Using cache
 ---> 786ff553c2d4
Step 3/8 : COPY requirements.txt /usr/src/app/
 ---> Using cache
 ---> b209c4e10615
Step 4/8 : RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt
 ---> Running in 86fb2f68f11f
Collecting Flask==1.0 (from -r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/55/b1/4365193655df97227ace49311365cc296e74b60c7f5c63d23cd30175e2f6/Flask-1.0-py2.py3-none-any.whl (97kB)
Collecting itsdangerous>=0.24 (from Flask==1.0->-r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/76/ae/44b03b253d6fade317f32c24d100b3b35c2239807046a4c953c7b89fa49e/itsdangerous-1.1.0-py2.py3-none-any.whl
Collecting Jinja2>=2.10 (from Flask==1.0->-r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/7e/c2/1eece8c95ddbc9b1aeb64f5783a9e07a286de42191b7204d67b7496ddf35/Jinja2-2.11.3-py2.py3-none-any.whl (125kB)
Collecting Werkzeug>=0.14 (from Flask==1.0->-r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/cc/94/5f7079a0e00bd6863ef8f1da638721e9da21e5bacee597595b318f71d62e/Werkzeug-1.0.1-py2.py3-none-any.whl (298kB)
Collecting click>=5.1 (from Flask==1.0->-r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/d2/3d/fa76db83bf75c4f8d338c2fd15c8d33fdd7ad23a9b5e57eb6c5de26b430e/click-7.1.2-py2.py3-none-any.whl (82kB)
Collecting MarkupSafe>=0.23 (from Jinja2>=2.10->Flask==1.0->-r /usr/src/app/requirements.txt (line 1))
  Downloading https://files.pythonhosted.org/packages/b9/2e/64db92e53b86efccfaea71321f597fa2e1b2bd3853d8ce658568f7a13094/MarkupSafe-1.1.1.tar.gz
Installing collected packages: itsdangerous, MarkupSafe, Jinja2, Werkzeug, click, Flask
  Running setup.py install for MarkupSafe: started
    Running setup.py install for MarkupSafe: finished with status 'done'
Successfully installed Flask-1.0 Jinja2-2.11.3 MarkupSafe-1.1.1 Werkzeug-1.0.1 click-7.1.2 itsdangerous-1.1.0
You are using pip version 9.0.0, however version 23.0 is available.
You should consider upgrading via the 'pip install --upgrade pip' command.
Removing intermediate container 86fb2f68f11f
 ---> eb724b51d9d9
Step 5/8 : COPY app.py /usr/scr/app/
 ---> 1b7debb4b399
Step 6/8 : COPY templates/index.html /usr/src/app/templates/
 ---> 9b9293930845
Step 7/8 : EXPOSE 5000
 ---> Running in 121f758548c8
Removing intermediate container 121f758548c8
 ---> e0c04cd60633
Step 8/8 : CMD ["python","/usr/src/app/app.py"]
 ---> Running in 6541f74b8ade
Removing intermediate container 6541f74b8ade
 ---> 089525bb1e3a
Successfully built 089525bb1e3a
Successfully tagged myfirstapp:1.01

``` 
6. verify the docker image 
```bash
root@ubuntu:/home/ptiwari/gitrepo/Docker-learning/Assignment/flask-app# docker images
REPOSITORY                  TAG          IMAGE ID       CREATED              SIZE
myfirstapp                  1.01         089525bb1e3a   About a minute ago   57.2MB
```
7. run the docker image
```bash
root@ubuntu:/home/ptiwari/gitrepo/Docker-learning/Assignment/flask-app# docker run -p 5050:5000 myfirstapp:1.01
 * Serving Flask app "app" (lazy loading)

```