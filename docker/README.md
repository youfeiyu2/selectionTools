Ubuntu 14.04
=============

To be able to create a docker container with selectionTools inside it:
(currently need sudo access)
Install docker
see https://docs.docker.com


Build the docker image:
selectionTools/docker is the path to the directory containing the dockerfile
$ sudo docker build -t selectiondocker/selectiontools selectionTools/docker/

This should build a docker image based from ubuntu 14.04 and install all pre-requisites and the selection pipeline itself


Login:
$ sudo docker run -t -i selectiondocker/selectiontools /bin/bash

To be able to side load your data in run:
$ sudo docker run -t -v <path to data on host>:/data -i selectiondocker/selectiontools /bin/bash

Your data will be found in /data


Test installation:
(logged into the docker image)
$ selection_pipeline -h

The selection pipeline directory will be located at /selectionTools

If that all succeeds you can continue the setup process from section 2.5 in the manual setting up reference files








