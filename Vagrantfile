# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  #config.vm.provider "virtualbox" do |vb|
    #   # Display the VirtualBox GUI when booting the machine
    #   vb.gui = true
    #
    #   # Customize the amount of memory on the VM:
    #   vb.memory = "1024"
    # end

  #config.vm.provision "shell", inline: <<-SHELL
  #  #apt-get update
  #  #/home/root
  #  curl -o actions-runner-linux-x64-2.294.0.tar.gz \
  #    -L https://github.com/actions/runner/releases/download/v2.294.0/actions-runner-linux-x64-2.294.0.tar.gz
  #  # Some comment
  #SHELL

  config.vm.provision "shell" do |s|
    s.path = "test-script.sh"
    s.privileged = false
    s.args = "ABBVHGGAKQKEQLLB7ULRJF3C4MHAK"
    s.env = {
      "TOKEN" => "ABBVHGGAKQKEQLLB7ULRJF3C4MHAK", 
      "SHA256" => "a19a09f4eda5716e5d48ba86b6b78fc014880c5619b9dba4a059eaf65e131780",
      "RUNNER_NAME" => "test-runner"
    }
    s.sensitive = true 
  end
end
