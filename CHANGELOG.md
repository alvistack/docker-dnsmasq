# Docker Image Packaging for Dnsmasq

## YYYYMMDD.Y.Z - TBC

### Major Changes

## 20210718.1.1 - 2021-07-18

### Major Changes

  - Upgrade minimal Ansible community package support to 4.2.0

## 20210602.1.1 - 2021-06-02

### Major Changes

  - Upgrade minimal Ansible support to 4.0.0

## 20210313.1.1 - 2021-03-13

### Major Changes

  - Bugfix [ansible-lint
    `namespace`](https://github.com/ansible-community/ansible-lint/pull/1451)
  - Bugfix [ansible-lint
    `no-handler`](https://github.com/ansible-community/ansible-lint/pull/1402)
  - Bugfix [ansible-lint
    `unnamed-task`](https://github.com/ansible-community/ansible-lint/pull/1413)
  - Change GIT tag as per Vagrant Box naming and versioning limitation

## 2.80-4alvistack16 - 2020-12-09

### Major Changes

  - Migrate from Travis CI to GitLab CI
  - Revamp with Packer

## 2.80-4alvistack13 - 2020-10-14

### Major Changes

  - Refine Molecule matrix

## 2.80-4alvistack11 - 2020-08-26

### Major Changes

  - Upgrade minimal Ansible Lint support to 4.3.2
  - Upgrade Travis CI test as Ubuntu Focal based
  - Upgrade minimal Ansible support to 2.10.0

## 2.80-4alvistack8 - 2020-06-10

### Major Changes

  - Revamp `create`, `side_effect`, `verify` and `destroy` logic
  - Replace `tini` with `catatonit`
  - Rename `post_tasks.yml` as `side_effect.yml`
  - Upgrade base image to Ubuntu 20.04

## 2.79-4alvistack4 - 2020-03-05

### Major Changes

  - Revamp with Molecule and `docker commit`
  - Consolidate molecule tests into `default` (noop)
  - Hotfix for systemd

## 2.79-3alvistack1 - 2020-01-15

### Major Changes

  - Replace `dumb-init` with `tini`, as like as `docker --init`
  - Include release specific vars and tasks

## 2.79-2alvistack3 - 2019-11-05

### Major Changes

  - Upgrade minimal Ansible support to 2.9.0
  - Upgrade Travis CI test as Ubuntu Bionic based
  - Default with Python 3
  - Hotfix for en\_US.utf8 locale

## 2.79-0alvistack1 - 2019-09-10

  - Ubuntu 18.04 based
  - Handle ENTRYPOINT with dumb-init
  - Self initialize with Ansible, by dogfooding with Ansible Playbook
