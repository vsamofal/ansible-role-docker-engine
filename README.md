# Ansible Role: docker-engine [![Build Status](https://travis-ci.org/pauvos/ansible-role-docker-engine.svg?branch=master)](https://travis-ci.org/pauvos/ansible-role-docker-engine)

Installs docker-engine with official packages from [dockerproject.org](https://dockerproject.org/).

Tested with:

* CentOS 7
* Debian 8
* Fedora 24
* Ubuntu 16.04

## Get the role

    ansible-galaxy install pauvos.docker-engine

## Example Playbook

    ---
    - hosts: docker-hosts
      become: true
      roles:
        - { role: pauvos.docker-engine }

## Role Variables

Available variables are listed below, along with default values:

    docker_engine_cache_valid_time: 84600   # cache_valid_time for apt
