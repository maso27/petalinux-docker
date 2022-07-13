# petalinux-docker

Copy petalinux-v2021.1-final-installer.run file to this folder. Then run:

`docker build --build-arg PETA_VERSION=2021.1 --build-arg PETA_RUN_FILE=petalinux-v2021.1-final-installer.run -t petalinux:2021.1 .`

After installation, launch petalinux with:

`docker run -ti --rm -e DISPLAY=$DISPLAY --net="host" -v /tmp/.X11-unix:/tmp/.X11-unix -v $HOME/.Xauthority:/home/plx/.Xauthority -v $HOME/Projects:/home/plx/project  petalinux:2021.1 /bin/bash`
