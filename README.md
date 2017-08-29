# Ansible Role: docker-engine [![Build Status](https://travis-ci.org/pauvos/ansible-role-docker-engine.svg?branch=master)](https://travis-ci.org/pauvos/ansible-role-docker-engine)

Installs *docker-ce* with official packages from [download.docker.com](https://download.docker.com/).

Tested with:

* CentOS 7
* Debian 8
* Fedora 24
* Ubuntu 16.04

## Install
You can create requirements.yml and add these line there: 

---
    - src: https://github.com/vsamofal/ansible-role-docker-engine.git
      name: docker-engine
      version: master
      path: roles/docker-engine

Run install process like this: 

---
    ansible-galaxy install -r requirements.yml --roles-path roles/
    
    
## Example Playbook

    ---
    - hosts: docker-hosts
      become: true
      roles:
        - { role: pauvos.docker-engine }

## Role Variables

Available variables are listed below, along with default values:

    docker_engine_cache_valid_time: 84600   # cache_valid_time for apt
