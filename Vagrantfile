# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  
  config.vm.define "jenkinsMaster" do |jenkinsMaster|
     jenkinsMaster.vm.hostname = "jenkinsMaster"
     jenkinsMaster.vm.network "private_network", ip: "10.0.3.111"
     config.vm.provision :shell, :inline => "sudo apt-get update;
       sudo locale-gen de_DE.UTF-8
     "
  end
end
