docker-bio-linux8
=================

Dockerfile to build a container with Bio-Linux8 packages installed.

To build type:

```
git clone git@github.com:gawbul/docker-bio-linux8.git
cd docker-bio-linux8
(uncomment line 81 #RUN /bin/bash $HOME/bl_install_master_list.sh in the Dockerfile to install all Bio-Linux applications)
docker build -t gawbul/docker-bio-linux8 .
```

To pull from the Docker Hub (without packages installed) type:

```
docker pull gawbul/docker-bio-linux8
```

**NB**: Packages aren't installed as the automated build in Docker Hub times out when uploading the built image due to the size of the resulting image (~6GB)

To run the image in a container type:

```
docker run -it gawbul/docker-bio-linux8 bash
```

To run the image in a container with a mounted data folder (where /home/user/data is the path to your local data folder) type:

```
docker run -it -v /home/user/data:/home/biolinux/data gawbul/docker-bio-linux8 bash
```

**NB**: The default root password for mysql-server is root.
