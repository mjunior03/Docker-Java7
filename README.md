# Docker-Java7
Instantiate containers [Docker](http://docs.docker.io/ "Docker") using Java 1.7.

For this we will use Docker remote API [v1.19](https://github.com/docker/docker/blob/master/docs/reference/api/docker_remote_api_v1.19.md), Docker Server version 1.6.2.

##### Docker network configuration.

By default Docker server is using UNIX sockets for communication with the Docker client, however docker-java
client uses TCP/IP to connect to the Docker server by default, so you will need to make sure that your Docker server is
listening on TCP port. To allow Docker server to use TCP add the following line to /etc/default/docker

    DOCKER_OPTS="-H tcp://localhost:4243 -H unix:///var/run/docker.sock"

The image Docker used was "dockergui3". This is an image that brings an instance Firefox.

##### Docker from a distance - The remote API



