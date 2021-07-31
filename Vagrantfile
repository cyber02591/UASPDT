# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.define "web-server" do |vm1|
    vm1.vm.hostname = "web-server"
    vm1.vm.box = "hashicorp/precise64"
    vm1.vm.network "private_network", ip: "192.168.2.10"

    vm1.vm.provider "virtualbox" do |vb|
      vb.name = "web-server"
      vb.gui = false
      vb.memory = "1024"
    end  

    vm1.vm.provision "shell", inline:<<-SHELL 
      echo "Welcome to web-server VM"
      SHELL
    end

  config.vm.define "database-server" do |vm2|
    vm2.vm.hostname = "deb-server"
    vm2.vm.box = "hashicorp/precise64"
    vm2.vm.network "private_network", ip: "192.168.2.11"

    vm2.vm.provider "virtualbox" do |vb|
      vb.name = "deb-server"
      vb.gui = false
      vb.memory = "1024"
    end

    vm2.vm.provision "shell", inline:<<-SHELL 
      echo "Welcome to db-server VM"
      SHELL
    end

end