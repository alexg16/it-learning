# Containers

## Docker

- [The Docker Handbook](https://www.freecodecamp.org/news/the-docker-handbook/)
- [Back to Basics: Top Useful Docker Commands](https://adamtheautomator.com/back-to-basics-top-useful-docker-commands/)
- [dockerd configuration file](https://docs.docker.com/engine/reference/commandline/dockerd/)
- [Install Docker compose](https://docs.docker.com/compose/install/)
- [Manage data in Docker](https://docs.docker.com/engine/admin/volumes/)
- [The base command for the Docker CLI](https://docs.docker.com/engine/reference/commandline/docker/)
- [Easily Host an Awesome Docker Registry at Home](https://medium.com/@lukebenson/easily-host-an-awesome-docker-registry-at-home-694a9c70740f)

"""/mnt/registry:/var/lib/registry"""

- [Deploy a registry server](https://docs.docker.com/registry/deploying/)
- [How to get a list of images on docker registry v2](https://stackoverflow.com/questions/31251356/how-to-get-a-list-of-images-on-docker-registry-v2)
- [Create a service which creates an NFS volume](https://docs.docker.com/storage/volumes/#create-a-service-which-creates-an-nfs-volume)
- [Docker Swarm Persistent Storage with NFS](https://sysadmins.co.za/docker-swarm-persistent-storage-with-nfs/)
- [Netshare by ContainX](http://netshare.containx.io/docs/getting-started) and [github repository](https://github.com/ContainX/docker-volume-netshare)


### Compose

- [Compose file version 3 reference](https://docs.docker.com/compose/compose-file/)

## Linux

- Install Docker on Linux:

```
apt-get update
wget -qO- https://get.docker.com | sh
```

- Add loggedin user to docker group:

```
sudo gpasswd -a $USER docker
```
  re-login with new group membership:
```
newgrp docker
```

## Windows

- [Install Docker on Windows Server 2019](https://www.ntweekly.com/2018/11/03/install-docker-on-windows-server-2019/)
- [What's new for Docker on Windows Server 2019?](https://stefanscherer.github.io/docker-on-windows-server-2019/)
- [Pull WindowsServerCore Container Image](https://hub.docker.com/r/microsoft/windowsservercore/)
- [Linux Containers on Windows](https://docs.microsoft.com/en-us/virtualization/windowscontainers/deploy-containers/linux-containers)
- [Setup Docker on Windows Server 2016](https://blogs.technet.microsoft.com/canitpro/2016/10/26/step-by-step-setup-docker-on-your-windows-2016-server/)
- [Windows Containers Documentation](https://docs.microsoft.com/en-us/virtualization/windowscontainers/)

## Videos

- Containers? So What? Docker 101 Explained - Computer Stuff They Didn't Teach You #8

[![IMAGE ALT TEXT HERE](http://img.youtube.com/vi/0oEsMwSxBsk/default.jpg)](https://www.youtube.com/watch?v=0oEsMwSxBsk)
