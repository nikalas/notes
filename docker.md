Notes about Docker
==================

Connect to docker from within docker
------------------------------------

To connect to docker from inside a container you can bind mount the docker binary from the host to the container (usually /usr/bin/docker.sock)

Do note that this usually lets you run commands with root privileges. i.e. NOT SECURE.

More info at:
[forums.docker.com](https://forums.docker.com/t/how-can-i-run-docker-command-inside-a-docker-container/337/7)

Discussions at:
[github.com/docker](https://github.com/docker/docker/issues/1143)


Docker in Babun
---------------

To use Docker in [Babun][babun] on windows you need `winpty` which comes pre-installed in the package [babun-docker][babun-docker].

[docker]:       https://www.docker.com/
[babun]:        http://babun.github.io/
[babun-docker]: https://github.com/tiangolo/babun-docker
