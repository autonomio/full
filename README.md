# full
A docker container that starts with fully featured Autonomio augmented intelligence workbench with Keras/Tensorflow deep learning backend.


## Docker container contents

As a base image for the container we are using [phusion/baseimage](http://phusion.github.io/baseimage-docker/). You can find all the additions in the docker file. In addition to that there is a simplified access to container management. 

## Use of container management command

To simplify use in comparison to regular docker container user interface, we provide our own signle command and argument namespace. New creates a file 'current.id' which is then over-written by all the other commands so as long as destroy or new is called, the commands are "stuck" in the same container. This should minimize the possibility of deleting other containers by accident. 

To create a new container from image: 

    ./container new
    
To stop a running container: 

    ./container stop

To start a stopped container: 

    ./container start
    
To restart a container: 

    ./container restart 
    
To decomission a container: 

    ./container destroy
    
  