# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config| 
    config.vm.define :servidor1 do |servidor1| 
        servidor1.vm.box = "bento/ubuntu-22.04" 
        servidor1.vm.network :private_network, ip: "192.168.50.3" 
        servidor1.vm.hostname = "servidor1" 
        servidor1.vm.synced_folder "servidor1", "/vagrant",create: true
    end 
    config.vm.define :servidor2 do |servidor2| 
        servidor2.vm.box = "bento/ubuntu-22.04" 
        servidor2.vm.network :private_network, ip: "192.168.50.2" 
        servidor2.vm.hostname = "servidor2"
        servidor2.vm.synced_folder "servidor1", "/vagrant",create: true
    end 
end