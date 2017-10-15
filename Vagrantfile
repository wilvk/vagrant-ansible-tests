# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "fedora/26-cloud-base"
  if Vagrant::Util::Platform.windows? then
    config.vm.synced_folder ".", "/vagrant", type: "virtualbox"
  end
  config.vm.provision "shell", privileged: true,  inline: "yum -y install ansible"
  config.vm.provision "shell", privileged: false, inline: "ansible-playbook /vagrant/ansible/main.yml"
end
