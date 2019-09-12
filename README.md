# vagrant-xubuntu

Installing xubuntu on VirtualBox using vagrant 

# Prerequisites

- Virtual Box
  - Might be better to install it manually
- vagrant 
  - https://chocolatey.org/install
  - `choco install vagrant`

# Installation

- `git clone https://github.com/maxim-ge/vagrant-xubuntu.git`
- `vagrant up`
- Soon terminal appears
  - It is not the end, installation continues
- Log in/out using usr/pwd: vagrant
  - login prompt will be changed to `xubunty`
- When installation finished log in with usr/pwd: vagrant
- `startx`
- Enjoy
- BTW: you can run `double commander`

# Possible Next Steps

Installing Docker
- https://docs.docker.com/install/linux/docker-ce/ubuntu/

Adding `vagrant` to `docker` group (can run docker without `sudo`)
- `sudo usermod -a -G docker vagrant`
- Must log out/in
