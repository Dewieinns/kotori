#########################
Build Kotori using Docker
#########################

.. highlight:: bash


***
Run
***
Build Docker images::

    make build-debian-stretch-amd64-baseline
    make build-debian-stretch-armhf-baseline

Build Kotori package::

    # amd64
    make debian-package flavor=full arch=amd64 version=0.21.1

    # armhf
    make debian-package flavor=standard arch=armhf version=0.21.1


********
Research
********
- https://www.ecliptik.com/Cross-Building-and-Running-Multi-Arch-Docker-Images/
- https://docs.docker.com/develop/develop-images/multistage-build/

::

    docker run -it --rm arm32v7/debian:stretch-slim uname -a
    docker run -it --rm balenalib/armv7hf-debian:stretch-build uname -a