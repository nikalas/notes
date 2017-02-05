Notes about Docker
==================

Running commands on an already running container
------------------------------------------------

`docker exec container-name` lets you run commands on a running container

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

Logging
-------

Docker can handle the logs from your containers. It does this by reading the `STDOUT` on the container, so make sure your server or process logs to STDOUT (in the container). Docker can then write those log entries to syslog or another local service running on the host, or you can use a third party service such as Loggly(?).
