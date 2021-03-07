# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define :cliente do |cliente|
    cliente.vm.box = "bento/centos-7.9"
    cliente.vm.network :private_network, ip: "192.168.50.2"
    cliente.vm.hostname = "cliente"
  end
  
  config.vm.define :servidor do |servidor|
    servidor.vm.box = "bento/centos-7.9"
    servidor.vm.network :private_network, ip: "192.168.50.3"
    servidor.vm.hostname = "servidor"
    servidor.vm.network "forwarded_port", guest: 80, host: 5080
  end

  config.vm.synced_folder "./prueba_sinc","/home/vagrant/prueba_sinc",type:"virtualbox"

end
