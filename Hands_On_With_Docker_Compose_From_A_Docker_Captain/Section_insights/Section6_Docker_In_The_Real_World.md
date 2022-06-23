## Sections Insights 

**Numbers of base image variation**
 
 1. Slim 

 2. Alpine

 3. Wheezy

 4. Onbuild

 5. Windowservercore

 - To make a directory to linux you will run "mkdir"

 **Creating a Dockerfile**
```
 FROM python:2.7-alpine

RUN mkdir /app
WORKDIR /app

COPY requirement.txt /app/requirement.txt
RUN pip install -r requirements.txt 

COPY . .

LABEL maintener="John Carl Sanico <johncarlsanico1998@gmail.com>"\
          version="1.0";

CMD flask run --host=0.0.0.0 --port=5000
```
Label - The label instruction expect you to pass tin the key and value.

Cmd - It defines the default command that will be run it's darker image could started.


**Build Push Docker Images**

- I learn how to build a docker images by going to terminal and go to my folder which is the  `/c/diveintodocker/diveintodocker/src/06-docker-in-the-real-world/03-creating-a-dockerfile-part-1`.

- Input `docker image -t web1` in terminal. 

- `docker image rm web1:1.0` This removes an imaged name which is the web1.

- `docker login` Log in to a docker.

**2 Types of network**

1. Lan - Local Area Network

2. Wan- Wide Area Network

**Sharing Data to a docker host**

- I learn how to link a data between two containers without having been touch in docker by using this language Javascript and CSS.

