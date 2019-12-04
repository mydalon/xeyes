# xeyes
Dockerfile for xeyes Image

This just creates a sample Docker Image to demonstrate how you can run X11 application with docker.

To run this, try:

docker run -d --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix --user $(id -u):$(id -g) -v /etc/passwd:/etc/passwd -v $HOME:$HOME mydalon/xeyes:1 xeyes

-v /etc/passwd:/etc/passwd and -v $HOME:$HOME are not necessary for xeyes, but would make sure your username is known and you have access to your home directory in the X11 application
