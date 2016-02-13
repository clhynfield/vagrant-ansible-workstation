# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "osx" do |osx|
    osx.vm.box = "elcapitan64"
    osx.vm.provision "shell", path: "bootstrap-ansible.sh"
  end
  config.vm.define "linux" do |linux|
    linux.vm.box = "centos/7"
    linux.vm.provision "shell", path: "bootstrap-ansible.sh"
  end
  config.vm.synced_folder ".", "/vagrant", type: "rsync"
end
