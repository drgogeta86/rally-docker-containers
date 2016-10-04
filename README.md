# rally-docker-containers

Dockerfiles to create rally containers for different [OpenStack RDO releases](https://www.rdoproject.org).
- rally-rdo-mitaka: Dockefile for RDO Mitaka release

## Building instructions

```
cd rally-rdo-mitaka
docker build -t jreypo/rally-rdo-mitaka .
```

You can also pull the container image directly from Docker Hub
```
docker pull jreypo/rally-rdo-mitaka
```
Finally create a directory to put your rally test files and run the container mapping that directory as a volume
```
mkdir ~/rally-home
docker run --name rally-mitaka -i -t -v ~/rally-home:/home/rally jreypo/rally-rdo-mitaka
```
