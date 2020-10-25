#!/usr/bin/env ruby

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "centos/7"
    config.vm.hostname = "ipresence"
    config.vm.network "private_network", ip: "172.30.1.5"

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "4024"
        vb.cpus = "1"
    end

    config.vm.provision "ansible_local" do |ansible|
        ansible.become = true
        ansible.verbose = "v"
        ansible.galaxy_role_file = "requirements.yml"
        ansible.galaxy_roles_path = ".ansible/galaxy-roles"
        ansible.provisioning_path = "/vagrant"
        ansible.playbook = "playbook.yml"
    end
end