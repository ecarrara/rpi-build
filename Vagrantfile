# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "private_network", ip: "192.168.33.11"

  config.vm.network "public_network"

  config.vm.provider "virtualbox" do |vbox|
    vbox.memory = "2048"
    vbox.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "infra/site.yml"
    ansible.inventory_path = "infra/hosts"
  end
end
