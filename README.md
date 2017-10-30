# Walrus
Walrus is my develop center in a [Docker](https://www.docker.com/) container. The name is inspired by Captain Flint's ship (Character of the [Treasure Island](http://robert-louis-stevenson.org/works/treasure-island-1883/), created by [Robert Louis Stevenson](http://robert-louis-stevenson.org/) in 1883)

This image has installed [Docker](https://www.docker.com/) and [Docker Compose](https://docs.docker.com/compose/) so you can launch containers with different applications or programming languages. Vim is the default editor.

This image is created from [Debian](http://debian.org), if you want to use the image generated with [Alpine Linux](https://alpinelinux.org/) use [walrus-alpine](https://github.com/irespaldiza/walrus-alpine).

### How to use this image
To run this image you have to expose the Docker socket to your Docker CI container, by bind-mounting it with the flag -v.
~~~ 
docker run -v /var/run/docker.sock:/var/run/docker.sock \
            -it irespaldiza/walrus
~~~

It is designed to share a folder with our settings and resources. 
~~~ 
docker run -v /var/run/docker.sock:/var/run/docker.sock \
            -v pathToYourFolder:/root \
            -it irespaldiza/walrus
~~~
> In the git hub repository there is a folder called root with a simple configuration of bash vim and where I will be placing some files to launch applications with Docker Compose.
#### Alias 
In the .bashrc the following aliases have been added:
~~~
alias ll='ls -alF'
alias ls='ls --color=auto'
alias dk='docker'
~~~
> In the future, more aliases will be added in this file.
