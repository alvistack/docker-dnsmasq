# Docker Image Packaging for Dnsmasq

[![GitLab pipeline status](https://img.shields.io/gitlab/pipeline/alvistack/docker-dnsmasq/master)](https://gitlab.com/alvistack/docker-dnsmasq/-/pipelines)
[![GitHub release](https://img.shields.io/github/release/alvistack/docker-dnsmasq.svg)](https://github.com/alvistack/docker-dnsmasq/releases)
[![GitHub license](https://img.shields.io/github/license/alvistack/docker-dnsmasq.svg)](https://github.com/alvistack/docker-dnsmasq/blob/master/LICENSE)
[![Docker Pulls](https://img.shields.io/docker/pulls/alvistack/dnsmasq-2.80.svg)](https://hub.docker.com/r/alvistack/dnsmasq-2.80)

Dnsmasq provides network infrastructure for small networks: DNS, DHCP, router advertisement and network boot.

Learn more about Dnsmasq: <http://www.thekelleys.org.uk/dnsmasq/doc.html>

## Supported Tags and Respective Packer Template Links

  - [`alvistack/dnsmasq-2.80`](https://hub.docker.com/r/alvistack/dnsmasq-2.80)
      - [`packer/docker-2.80/packer.json`](https://github.com/alvistack/docker-dnsmasq/blob/master/packer/docker-2.80/packer.json)

## Overview

This Docker container makes it easy to get an instance of Dnsmasq up and running.

Based on [Official Ubuntu Docker Image](https://hub.docker.com/_/ubuntu/) with some minor hack:

  - Packaging by Packer Docker builder and Ansible provisioner in single layer
  - Handle `ENTRYPOINT` with [catatonit](https://github.com/openSUSE/catatonit)

### Quick Start

Start Dnsmasq:

    # Pull latest image
    docker pull alvistack/dnsmasq-2.80
    
    # Run as detach
    docker run \
        -itd \
        --cap-add NET_ADMIN \
        --name dnsmasq \
        --publish 53:53/udp \
        alvistack/dnsmasq-2.80
    
    # Run with custom /etc/dnsmasq.conf
    docker run \
        -itd \
        --cap-add NET_ADMIN \
        --name dnsmasq \
        --publish 53:53/udp \
        --volume /etc/dnsmasq.conf:/etc/dnsmasq.conf \
        alvistack/dnsmasq-2.80

**Success**. Dnsmasq is now available on port `53/udp`.

## Versioning

### `YYYYMMDD.Y.Z`

Release tags could be find from [GitHub Release](https://github.com/alvistack/docker-dnsmasq/releases) of this repository. Thus using these tags will ensure you are running the most up to date stable version of this image.

### `YYYYMMDD.0.0`

Version tags ended with `.0.0` are rolling release rebuild by [GitLab pipeline](https://gitlab.com/alvistack/docker-dnsmasq/-/pipelines) in weekly basis. Thus using these tags will ensure you are running the latest packages provided by the base image project.

## License

  - Code released under [Apache License 2.0](LICENSE)
  - Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

## Author Information

  - Wong Hoi Sing Edison
      - <https://twitter.com/hswong3i>
      - <https://github.com/hswong3i>
