# vagrant-xubuntu

Installing ubuntu/xubuntu on VirtualBox using vagrant 

# Prerequisites

- Virtual Box
  - https://www.virtualbox.org/wiki/Downloads
  - Better to install Virtual Box manually?
- vagrant 
  - Install choco https://chocolatey.org/install
  - `choco install vagrant`

# Installing xubuntu

- Change `username` variable in `./Vagrantfile`
- `vagrant up`
- Soon terminal appears
  - It is not the end, installation continues
- When installation finished sign in using `$username` and password `q'
- !!! Reboot machine
- `startx`
- Enjoy
- BTW: you can run `double commander`

# Installing ubuntu-cli

cd ubunti-cli
vagrant up
vagrant ssh


# Possible Next Steps

Changing Default Shell
- sudo chsh -s /bin/bash #{username}

Installing Docker
- https://docs.docker.com/install/linux/docker-ce/ubuntu/
