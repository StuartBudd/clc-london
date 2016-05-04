Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false

  # update all boxes on first start and fix locales
  config.vm.provision :shell, :inline => "apt-get update; locale-gen de_DE.UTF-8 en_US.UTF-8"

  config.vm.define "master" do |master|
    master.vm.provider "virtualbox" do |v|
      v.memory = 1536
      v.cpus = 2
    end
    master.vm.hostname = "jenkins-master"
    master.vm.network "private_network", ip: "10.0.3.111"
  end

  config.vm.define "slave1" do |slave1|
    slave1.vm.hostname = "jenkins-slave1"
    slave1.vm.network "private_network", ip: "10.0.3.112"
  end

end
