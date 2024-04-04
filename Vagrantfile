# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "geerlingguy/ubuntu2004"
  #config.vm.box = "geerlingguy/rockylinux8"
  config.vm.synced_folder '.', '/vagrant', disabled: true
  config.vm.network "forwarded_port", guest: 80, host: 20080
  config.ssh.insert_key = false

  config.vm.provider "virtualbox" do |v|
    v.name = "zabbix"
    v.memory = 1024
    v.cpus = 1
  end

  # Provisioning configuration for Ansible.
  config.vm.provision "ansible" do |ansible|
    #ansible.verbose = "vvv"
    ansible.playbook = "main.yml"
  end
end
