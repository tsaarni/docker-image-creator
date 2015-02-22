
# docker-image-creator container appliance

This Docker image is intended to be called through script
`docker-image-creator` which you can download here
https://github.com/tsaarni/docker-image-creator.

The image has an entrypoint that calls
[ami-creator](https://github.com/katzj/ami-creator) for building
filesystem image from kickstart file.  After the image
has been successfully built, it converts the resulting filesystem
image to Docker base image.

For more information on how this works, see *CentOS Docker build
scripts*
https://github.com/CentOS/sig-cloud-instance-build/tree/master/docker.
