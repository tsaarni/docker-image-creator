
# docker-image-creator

`docker-image-creator` is a convenience script which creates
CentOS / Fedora / Red Hat -style Docker base images.

The script relies on
[ami-creator](https://github.com/katzj/ami-creator) and Docker itself
to build the images, however you only need Docker installed in your
system, since the building is executed in fully self-containing Docker
appliance.


### Usage

    docker-image-creator kickstart-file image-name


### Examples

    wget https://raw.githubusercontent.com/CentOS/sig-cloud-instance-build/master/docker/centos-7.ks
    docker-image-creator centos-7.ks centos-7


### Further information

* [CentOS Docker build scripts](https://github.com/CentOS/sig-cloud-instance-build/tree/master/docker) - kickstart files
* [ami-creator](https://github.com/katzj/ami-creator) - used to create the images
* [sle2docker](https://github.com/SUSE/sle2docker) - motivator for creating this script

