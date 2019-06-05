# development-machine

Ansible scripts that I use to setup my development machine.

## Overview

This bootstraps a bare install of Ubuntu 18.04 (with ssh keys already installed, but nothing else) and will install the following:

-   [Docker](https://www.docker.com/)
-   [PHP](https://php.net/)
    -   [Composer](https://getcomposer.org/)
-   [Nginx](https://www.nginx.com/)
-   [Mysql Server](https://dev.mysql.com/)
-   [PostgrSQL](https://www.postgresql.org/)
-   [NVM](https://github.com/nvm-sh/nvm)
-   [Memcached](https://memcached.org/)
-   [Redis](https://redis.io/)
-   [Beanstalkd](https://beanstalkd.github.io/)
-   [MailHog](https://github.com/mailhog/MailHog)
-   [AWS CLI](https://aws.amazon.com/cli/)
-   [My dotfiles](https://github.com/RyanTheAllmighty/dotfiles)

## Prerequisites

In order to run this, you'll need:

-   A server running [Ubuntu Server 18.04](https://www.ubuntu.com/download/server)
-   [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed on your local machine

## Running

First you need to install the requirements from Ansible galaxy by running:

```sh
ansible-galaxy install -r requirements.yml
```

Now check you can ping the host:

```sh
ansible -i "HOSTNAME-OR-IP-HERE," -m ping
```

To run the scripts, simply run:

```sh
ansible-playbook -i "HOSTNAME-OR-IP-HERE," setup.yml -v -K
```

## Why

I run my main desktop as a VM which causes issues with running applications such as Docker and Vagrant. Also wanting to use [VSCode Remote Development](https://code.visualstudio.com/docs/remote/ssh) to have a stable development environment that can be run on any machine.
