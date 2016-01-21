# -*- mode: ruby -*-
# vi: set ft=ruby :

# Tested with Arch Linux 64-bit 4.3.3

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "lab-ckan" do |lab|
    lab.vm.box = "mjp182/CentOS_7"
    lab.vm.network :private_network, ip: "10.0.0.10"
    lab.vm.synced_folder "./src", "/sources"

    lab.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/playbook.yml"
      ansible.verbose = "v"
      ansible.limit = "webserver"
      ansible.inventory_path = "vagrant-ansible-inventory"
    end
  end
end
