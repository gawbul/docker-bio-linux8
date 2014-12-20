docker-bio-linux8
=================

Dockerfile to build a container with Bio-Linux8 packages installed.

To build type:

```
git clone git@github.com:gawbul/docker-bio-linux8.git
cd docker-bio-linux8
docker build -t gawbul/docker-bio-linux8 .
```

To pull from the Docker Hub type:

```
docker pull gawbul/docker-bio-linux8
```

To run the image in a container type:

```
docker run -it --rm gawbul/docker-bio-linux8 bash
```

**NB**: The default root password for mysql-server is root.
