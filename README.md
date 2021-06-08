# dockerfile
Host all the docker file used in the `svalinn` workflows, CI....

Pushing to the main branch of this repository triggers a rebuild of all
dockerfiles in the repository and publishing of the resulting docker images on
the [Svalinn DockerHub](https://hub.docker.com/u/svalinn) with the tags:

- [pymoab-py2-18.04](https://hub.docker.com/r/svalinn/pymoab-py2-18.04)
- [pymoab-py3-18.04](https://hub.docker.com/r/svalinn/pymoab-py2-18.04)
- [pymoab-visit-py2-18.04](https://hub.docker.com/r/svalinn/pymoab-py2-18.04)
