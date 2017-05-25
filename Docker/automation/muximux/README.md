# Muximux

A simple reverse proxy to manage internal network resources.

Dockerfile build based on ioft/armhf-ubuntu
Built using a Raspberry Pi 2b
Running Ubuntu 16.04.1 LTS (GNU/Linux 4.4.0-1050-raspi2 armv7l)

Uses onedr0p's implementation of the Managethis/Muximux project via nodejs.
https://github.com/onedr0p/manage-this-node

Steps:

1. Install docker
2. initialize build folder
3. git clone https://github.com/agitham/armv7.git
4. docker build -t <dockername>/muximux .
5. docker run --name muximux_00 -p 8080:3000 -id <dockername>/muximux
