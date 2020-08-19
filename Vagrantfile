username = "maxim-ge"

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/bionic64"
  config.vm.hostname = "xubuntu-bionic-2"



  config.vm.provider "virtualbox" do |vb|
    vb.name = "xubuntu-bionic-2"
	vb.memory = "2800"
    vb.gui = true
    vb.customize ["modifyvm", :id, "--vram", "128"]
    # Clipboard enabled
    vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
    vb.customize ["modifyvm", :id, "--draganddrop", "hosttoguest"]
  end

  # Create user
  config.vm.provision "shell", inline: "sudo useradd -p \"\" #{username} -m -G sudo"
  config.vm.provision "shell", inline: "sudo chsh -s /bin/bash #{username}"
  config.vm.provision "shell", inline: "sudo echo '#{username}:q' | sudo chpasswd"

  # Install xfce and virtualbox additions
  config.vm.provision "shell", inline: "sudo apt-get update"
  config.vm.provision "shell", inline: "sudo apt-get install -y xfce4 doublecmd-gtk virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11"

  # git gui
  config.vm.provision "shell", inline: "sudo apt-get install -y git-gui"

  # Permit anyone to start the GUI
  config.vm.provision "shell", inline: "sudo sed -i 's/allowed_users=.*$/allowed_users=anybody/' /etc/X11/Xwrapper.config"
end

# Links
# https://github.com/chocolatey-community/chocolatey-test-environment/blob/master/Vagrantfile
