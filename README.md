# vagrant-xubuntu

Installing xubuntu on VirtualBox using vagrant 

# Prerequisites

- https://chocolatey.org/install
- Virtual Box
  - Might be better to install it manually
- vagrant 
  - `choco install vagrant`

# Installation

- `git clone https://github.com/maxim-ge/vagrant-xubuntu.git`
- `vagrant up`
- soon terminal appears
  - It is not the end, installation continues
- log in/out using usr, pwd: vagrant
  - login prompt will be change to `xubunty`
- When installation finished log in with usr, pwd: vagrant
- `startx`
- enjoy
- Btw: you can run `double commander`

# Possible Next Steps

Installing Docker
- https://docs.docker.com/install/linux/docker-ce/ubuntu/

Adding `vagrant` to `docker` group (can run docker without `sudo`)
- `sudo usermod -a -G docker vagrant`
- Must log out/in
