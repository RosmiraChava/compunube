# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  if Vagrant.has_plugin? "vagrant-vbguest"
    config.vbguest.no_install  = true
    config.vbguest.auto_update = false
    config.vbguest.no_remote   = true
  end

    #config.vm.define :nodo2 do |nodo2|
    #nodo2.vm.box = "bento/ubuntu-22.04"
    #nodo2.vm.network :private_network, ip: "192.168.100.4"
    #nodo2.vm.hostname = "nodo2"
    #nodo2.vm.provision "shell", path: "scriptnodo2.sh"
  #end

    config.vm.define :clienteUbuntu do |clienteUbuntu|
    clienteUbuntu.vm.box = "bento/ubuntu-22.04"
    clienteUbuntu.vm.network :private_network, ip: "192.168.100.2"
    clienteUbuntu.vm.hostname = "clienteUbuntu"
    clienteUbuntu.vm.provision "shell", path: "scriptcliente.sh"	
  end

  config.vm.define :servidorUbuntu do |servidorUbuntu|
    servidorUbuntu.vm.box = "bento/ubuntu-22.04"
    servidorUbuntu.vm.network :private_network, ip: "192.168.100.3"
    servidorUbuntu.vm.hostname = "servidorUbuntu"
    servidorUbuntu.vm.provision "shell", path: "scriptservidor.sh"
   
  end
end
