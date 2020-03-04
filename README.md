# Docker Image Packaging for Dnsmasq

[![Travis](https://img.shields.io/travis/alvistack/docker-dnsmasq.svg)](https://travis-ci.org/alvistack/docker-dnsmasq)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-dnsmasq.svg)](https://github.com/alvistack/docker-dnsmasq/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-dnsmasq.svg)](https://github.com/alvistack/docker-dnsmasq/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/dnsmasq.svg)](https://hub.docker.com/r/alvistack/dnsmasq/)

Dnsmasq provides network infrastructure for small networks: DNS, DHCP, router advertisement and network boot.

Learn more about Dnsmasq: <http://www.thekelleys.org.uk/dnsmasq/doc.html>

## Supported Tags and Respective `Dockerfile` Links

  - [`2.79`, `latest`](https://github.com/alvistack/docker-dnsmasq/blob/master/molecule/2.79/Dockerfile.j2)

## Overview

This Docker container makes it easy to get an instance of Dnsmasq up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Minimized `Dockerfile` for meta data definition
  - Provision by Ansible and Molecule Docker driver in single layer
  - Handle `ENTRYPOINT` with [tini](https://github.com/krallin/tini)

### Quick Start

Start Dnsmasq:

    # Pull latest image
    docker pull alvistack/dnsmasq
    
    # Run as detach
    docker run \
        -itd \
        --cap-add NET_ADMIN \
        --name dnsmasq \
        --publish 53:53/udp \
        alvistack/dnsmasq
    
    # Run with custom /etc/dnsmasq.conf
    docker run \
        -itd \
        --cap-add NET_ADMIN \
        --name dnsmasq \
        --publish 53:53/udp \
        --volume /etc/dnsmasq.conf:/etc/dnsmasq.conf \
        alvistack/dnsmasq

**Success**. Dnsmasq is now available on port `53/udp`.

## Versioning

The `latest` tag matches the most recent [GitHub Release](https://github.com/alvistack/docker-dnsmasq/releases) of this repository. Thus using `alvistack/dnsmasq:latest` or `alvistack/dnsmasq` will ensure you are running the most up to date stable version of this image.

Other tags are rolling release rebuild by [Travis](https://travis-ci.org/alvistack/docker-dnsmasq) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
