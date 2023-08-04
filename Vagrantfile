# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM configuration.
  config.vm.box = "geerlingguy/rockylinux8"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.linked_clone = true
  end

  # Observer servers.
  config.vm.define "padok-observer" do |observer|
    observer.vm.hostname = "padok-observer.test"
    observer.vm.network :private_network, ip: "192.168.56.10"
  end

  # Target #1
  config.vm.define "padok-target-1" do |target|
    target.vm.hostname = "padok-target-1"
    target.vm.network :private_network, ip: "192.168.56.20"
  end

  # Target #2
  config.vm.define "padok-target-2" do |target|
    target.vm.hostname = "padok-target-2"
    target.vm.network :private_network, ip: "192.168.56.21"
  end
end
