
# docker-image-creator

`docker-image-creator` is a convenience tool which creates CentOS /
Fedora / Red Hat -style Docker base images.

The tool relies on
[ami-creator](https://github.com/katzj/ami-creator) and
[Docker](https://www.docker.com/) itself to build the images.  However
you only need Docker installed in your system since image is built inside
fully self-contained Docker container.


### Usage

    docker-image-creator kickstart-file image-name


### Example

    $ wget https://raw.githubusercontent.com/CentOS/sig-cloud-instance-build/master/docker/centos-7.ks
    $ docker-image-creator centos-7.ks centos-7
    $ docker import - my-centos7-base < centos-7.tar.xz
    $ docker run --rm -i -t my-centos7-base /bin/bash
    [root@1ecd80bd71e7 /]# cat /etc/redhat-release 
    CentOS Linux release 7.0.1406 (Core) 
    [root@1ecd80bd71e7 /]# 


### Further information

* [docker-image-creator container](https://registry.hub.docker.com/u/tsaarni/docker-image-creator/) - Docker container used by this tool
* [CentOS Docker build scripts](https://github.com/CentOS/sig-cloud-instance-build/tree/master/docker) - Original idea for this tool and ready-made kickstart files
* [ami-creator](https://github.com/katzj/ami-creator) - Basis for this tool, creates the image files
* [sle2docker](https://github.com/SUSE/sle2docker) - Inspiration for creating this tool

