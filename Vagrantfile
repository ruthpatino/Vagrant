# -*- mode: ruby -*-
# vi: set ft=ruby :
 
Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian9"
  config.vm.boot_timeout = 800
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.provision "shell", path: "setup.sh"
  config.vm.provider "virtualbox" do |v|
    v.name = "Vagrant"
    v.memory = 2048
    v.cpus = 2
  end  
end