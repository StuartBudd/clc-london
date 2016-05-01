# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false

  # update all boxes on first start and fix locales
  config.vm.provision :shell, :inline => "apt-get update; locale-gen de_DE.UTF-8 en_US.UTF-8"

  config.vm.define "master" do |jenkinsMaster|
    # Customize the amount of memory on the VM:
    jenkinsMaster.vm.hostname = "jenkins-master"
    jenkinsMaster.vm.network "private_network", ip: "10.0.3.111"
  end

  config.vm.define "slave1" do |jenkinsSlave|
    # Customize the amount of memory on the VM:
    jenkinsSlave.vm.hostname = "jenkins-slave1"
    jenkinsSlave.vm.network "private_network", ip: "10.0.3.112"
  end

end
