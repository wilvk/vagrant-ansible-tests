# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "fedora/26-cloud-base"
  config.vm.provision "shell", path: "run_ansible.sh", privileged: false
end
