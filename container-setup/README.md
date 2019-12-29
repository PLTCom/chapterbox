= README - Container Setup

== Architecture Overview

* Frontend Container: https://github.com/linuxserver/docker-letsencrypt or https://github.com/jwilder/nginx-proxy
* User DB: https://hub.docker.com/r/jboss/keycloak
* Document Storage: https://hub.docker.com/_/nextcloud w/fpm tag
* Chat: TBD

=== Runtimes
The containers will run using the Podman runtime. This makes it easier to run containers without root, as well as taking up less resources than the Docker engine. Ansible will be the orchestration tool, using systemd unit files to run containers as services. See https://redhatnordicssa.github.io/ansible-podman-containers-1.l