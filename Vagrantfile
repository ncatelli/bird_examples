# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "peer1" do |peer1|
    peer1.vm.box = "debian/stretch64"
    peer1.vm.hostname = "peer1"
    peer1.vm.network "private_network", ip: "10.0.0.10"
    peer1.vm.network "private_network", ip: "10.0.100.10"
    peer1.vm.provision "chef_zero" do |chef|
      chef.node_name = "peer1"
      chef.data_bags_path = "data_bags"
      chef.nodes_path = "nodes"
      chef.roles_path = "roles"
      chef.synced_folder_type = "rsync"
    end
  end

  config.vm.define "peer2" do |peer2|
    peer2.vm.box = "debian/stretch64"
    peer2.vm.hostname = "peer2"
    peer2.vm.network "private_network", ip: "10.0.0.11"
    peer2.vm.provision "chef_zero" do |chef|
      chef.node_name = "peer2"
      chef.data_bags_path = "data_bags"
      chef.nodes_path = "nodes"
      chef.roles_path = "roles"
      chef.synced_folder_type = "rsync"
    end
  end

  config.vm.define "peer3" do |peer3|
    peer3.vm.box = "debian/stretch64"
    peer3.vm.hostname = "peer3"
    peer3.vm.network "private_network", ip: "10.0.100.11"
    peer3.vm.provision "chef_zero" do |chef|
      chef.node_name = "peer3"
      chef.data_bags_path = "data_bags"
      chef.nodes_path = "nodes"
      chef.roles_path = "roles"
      chef.synced_folder_type = "rsync"
    end
  end
end
