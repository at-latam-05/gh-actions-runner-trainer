# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  config.vm.provider "virtualbox" do |vb|
       # Display the VirtualBox GUI when booting the machine
       vb.gui = true
    
       # Customize the amount of memory on the VM:
       vb.memory = "1024"
     end

  config.vm.provision "shell", inline: <<-SHELL
    #apt-get update
    #/home/root
    curl -o actions-runner-linux-x64-2.294.0.tar.gz \
      -L https://github.com/actions/runner/releases/download/v2.294.0/actions-runner-linux-x64-2.294.0.tar.gz
  SHELL
end
