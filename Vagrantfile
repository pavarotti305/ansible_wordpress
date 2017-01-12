# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # General Vagrant VM configuration.
  config.vm.box = "debian/jessie64"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider :virtualbox do |v|
    v.memory = 1000
    v.linked_clone = true
  end

  # Web server 1.
  config.vm.define "ditelk1" do |webservers|
    webservers.vm.hostname = "ditelkin1"
    webservers.vm.network "private_network", ip: "192.168.34.11"
  end

  # Monitor server 2.
  config.vm.define "ditelk2" do |monservers|
    monservers.vm.hostname = "ditelkin2"
    monservers.vm.network "private_network", ip: "192.168.34.12"
  end

  # Web server 3.
  config.vm.define "ditelk3" do |webservers|
    webservers.vm.hostname = "ditelkin3"
    webservers.vm.network "private_network", ip: "192.168.34.13"
  end

  # Web server 4.
  config.vm.define "ditelk4" do |webservers|
    webservers.vm.hostname = "ditelkin4"
    webservers.vm.network "private_network", ip: "192.168.34.14"
  end


  # Database server.
  config.vm.define "db_ditelk" do |dbservers|
    dbservers.vm.hostname = "ditelkin5"
    dbservers.vm.network "private_network", ip: "192.168.34.20"
  end
end