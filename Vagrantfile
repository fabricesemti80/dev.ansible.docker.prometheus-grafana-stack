# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant Linux VM configuration.
  config.vm.box = "geerlingguy/rockylinux8"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus = 3
    v.linked_clone = true
  end

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant Windows VM configuration.
  config.vm.box = "gusztavvargadr/windows-server-core"
  config.vm.communicator = "winrm"
  # config.winrm.username = "your_windows_username"
  # config.winrm.password = "your_windows_password"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus = 2
    v.linked_clone = true
  end
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
