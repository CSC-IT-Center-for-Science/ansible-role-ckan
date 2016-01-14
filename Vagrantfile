# -*- mode: ruby -*-
# vi: set ft=ruby :

# Tested with Arch Linux 64-bit 4.3.3

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define "lab-ckan" do |lab|
    lab.vm.box = "centos-7"
    lab.vm.box_url = "https://atlas.hashicorp.com/centos/boxes/7/versions/1509.01/providers/virtualbox.box"
    lab.vm.network :private_network, ip: "10.0.0.10"
    lab.vm.synced_folder "./src", "/sources"
  end
end
