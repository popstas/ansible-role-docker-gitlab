# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.provider "virtualbox" do |config|
    config.memory = 1024
  end

  #config.vm.provision "shell",
  #  inline: "apt-get -qq update && apt-get install -qq -y python-pip && pip install -q ansible"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "test.yml"
    #ansible.sudo = true
    ansible.verbose = "vvvv"
  end
end