# development-machine

Ansible scripts that I use to setup my development machine.

## Overview

This bootstraps a bare install of Ubuntu 18.04 (with ssh keys already installed, but nothing else) and will install the following:

- [PHP](https://php.net/)
  - [Composer](https://getcomposer.org/)
- [Nginx](https://www.nginx.com/)
- [Mysql Server](https://dev.mysql.com/)
- [NVM](https://github.com/nvm-sh/nvm)
- [Redis](https://redis.io/)
- [Beanstalkd](https://beanstalkd.github.io/)
- [My dotfiles](https://github.com/RyanTheAllmighty/dotfiles)

## Prerequisites

In order to run this, you'll need:

- A server running [Ubuntu Server 18.04](https://www.ubuntu.com/download/server)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed on your local machine

## Why

I run my main desktop as a VM which causes issues with running applications such as Docker and Vagrant. Also wanting to use [VSCode Remote Development](https://code.visualstudio.com/docs/remote/ssh) to have a stable development environment that can be run on any machine.
