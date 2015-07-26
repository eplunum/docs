![ePlunum](res/ePlunum-logo.png)

Copyright &copy; 2015. Dan Mascenik. All Rights Reserved.

# The Standalone Docker Container
[&laquo; Getting Started](getting-started.md)

The standalone Docker image is a great way to try out the ePlunum platform. It's also useful for offline testing of ePlunum applications. Please note, however, that the standalone container does not provide any persistent storage. All applications and execution states are lost when the container is shutdown.

Please note that depending on your platform, you may need to use ```sudo``` when running the following commands.

To pull down the latest image, check [Docker Hub](https://registry.hub.docker.com/u/eplunum/demo/tags/manage/) for the latest tagged version and run:

```
$ docker pull eplunum/demo:<version>
```

ePlunum exposes a single grid node on port 8080, so be sure to map that port to the Docker host's port 8080 with the ```-p``` flag as shown. To start the container streaming the server log to the terminal:

```
$ docker run -t -p 8080:8080 eplunum/demo:<version>
```
or optionally run the container in daemon mode:

```
$ docker run -d -p 8080:8080 eplunum/demo:<version>
```
