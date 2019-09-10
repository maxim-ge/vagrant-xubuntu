# 

Vagrant.configure(2) do |config|
  # Ubuntu 15.10
  config.vm.box = "bento/ubuntu-18.04"
  config.vm.hostname = "xubuntu"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "xubuntu"
	vb.memory = "2800"
    vb.gui = true
    vb.customize ["modifyvm", :id, "--vram", "128"]
    # Clipboard enabled
    vb.customize ["modifyvm", :id, "--clipboard", "bidirectional"]
    vb.customize ["modifyvm", :id, "--draganddrop", "hosttoguest"]
  end

  # Install xfce and virtualbox additions
  config.vm.provision "shell", inline: "sudo apt-get update"
  config.vm.provision "shell", inline: "sudo apt-get install -y xfce4 doublecmd-gtk virtualbox-guest-dkms virtualbox-guest-utils virtualbox-guest-x11"
  # Permit anyone to start the GUI
  config.vm.provision "shell", inline: "sudo sed -i 's/allowed_users=.*$/allowed_users=anybody/' /etc/X11/Xwrapper.config"
end

# Links
# https://github.com/chocolatey-community/chocolatey-test-environment/blob/master/Vagrantfile