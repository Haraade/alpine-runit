# This is a somewhat minimal image to use for your containers on arm32v7.

This is basically gliderlabs/alpine's Alpine Linux base image for arm32v7 with some modification. This adds runit + similar modifications as baseimage.There is a simpler startup mechanism than my_init. It relies on s simple shell script to dump the environment in /etc/envvars. All runit services you add need to source this file to gain access to the container environment. Similarly, instead of /etc/my_init.d for pre-service scripts to run, the startup shell script sequentially runs scripts found in /etc/runit_init.d.

Please feel free to use it or build upon it as needed. 

## License

[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](LICENSE)

Refer `LICENSE` file in this repository.

