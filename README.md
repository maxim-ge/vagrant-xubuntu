# vagrant-xubuntu

Installing xubuntu on VirtualBox using vagrant 

# Prerequisites

- Virtual Box
  - https://www.virtualbox.org/wiki/Downloads
  - Better to install Virtual Box manually?
- vagrant 
  - Install choco https://chocolatey.org/install
  - `choco install vagrant`

# Installation

- `git clone https://github.com/maxim-ge/vagrant-xubuntu.git`
- Change `username` variable in `Vagrantfile`
- `vagrant up`
- Soon terminal appears
  - It is not the end, installation continues
- When installation finished log in using `$username`
  - BTW: `$username` is added to `sudo` group
- `startx`
- Enjoy
- BTW: you can run `double commander`

# Possible Next Steps

Installing Docker
- https://docs.docker.com/install/linux/docker-ce/ubuntu/
