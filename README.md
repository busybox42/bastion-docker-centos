[![](https://images.microbadger.com/badges/image/busybox42/bastion-docker-centos.svg)](https://microbadger.com/images/busybox42/bastion-docker-centos "Get your own image badge on microbadger.com")
[![](https://images.microbadger.com/badges/version/busybox42/bastion-docker-centos.svg)](https://microbadger.com/images/busybox42/bastion-docker-centos "Get your own version badge on microbadger.com")
# bastion-docker-centos
This repository contains my CentOS bastion image.  This is a work in progress.

## Downloading the image
The first step is to pull the image.
```bash
docker pull busybox42/bastion-docker-centos
```

## Creating the container
Now that we have the image busybox42/bind-docker-centos we can create the container with a few parameters.
```bash
docker run --name admin -p 22:22 -h admin.myhost.tld busybox42/bastion-docker-centos
```
Name the container, expose port 22 for ssh and set a hostname.

## Configuring your server
You can connect to the container with this command:
```bash
docker exec -it bind bash
```
Update the config as necessary.
