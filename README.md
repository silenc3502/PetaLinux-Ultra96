# Dockerfile for Petalinux-Zybo-Z7-10

This is a Petalinux docker file for digilent Zybo Z7-10. You need to download petalinux 2017.4 from Xilinx. 

You can download the petalinux with aria2c which enables multipart download.

```
# aria2c -m 10 -s 10 -x 10 -o petalinux-v2017.4-final-installer.run <petalinux link>
```

## Building docker image
```
$ docker build --build-arg PETALINUX_INSTALLER=petalinux-v2017.4-final-installer.run -t petalinux .
```

## Run docker container
```
$ docker run -it -v <your directory>:/home/vivado/workshop petalinux
```