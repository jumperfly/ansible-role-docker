# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "jumperfly/centos-7-ansible"
  config.vm.box_version = "1804.02.01"
  config.vm.box_check_update = false
  config.ssh.insert_key = false
  config.vm.network "forwarded_port", guest: 2375, host: 2375

  config.vm.provider "virtualbox" do |v|
    v.memory = 512
    v.cpus = 1
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.playbook = "tests/vagrant-deps.yml"
  end

  config.vm.provision "ansible_local" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.playbook = "tests/test.yml"
  end
end
