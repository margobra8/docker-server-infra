
# docker-server-infra _(aka Hyperion)_
Docker-based infrastructure skeleton for my current personal server.

---

<img src="https://imgur.com/uIro3kT.png" width="100" align="left" />

My current server is based on a Linux machine running [Rocky Linux 8.5](https://rockylinux.org/), which is in turn based on RedHat Enterprise Linux 8.5.

Docker containers are run on a separate container virtual bridge and under a separate user with locked down privileges. The server most external routing layer has `iptables` configured to limit traffic to only allowed ports and under rate-limiting restrictions.

Some considerations:

- The containers are run with net isolation, i.e. each container is given its own network stack (ipv4 and ipv6) and its own hostname.

- The exposed containers or services are proxied through [traefik](https://doc.traefik.io/traefik/), an open source reverse proxy and loadbalancer.

- The internal containers and services are configured through docker-compose files.

> To-do : expand and develop README.md

Check all the docker-compose files for the different services in this project.

