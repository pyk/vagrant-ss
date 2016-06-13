# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "trusty64" do |trusty64|
    trusty64.vm.box = "ubuntu/trusty64"
    trusty64.vm.hostname = "ss"
    trusty64.vm.network "private_network", ip: "192.168.33.10"

    trusty64.vm.provider :virtualbox do |vb|
      vb.gui = false
      vb.memory = (1 * 2048)
      vb.cpus = 4
    end

    trusty64.vm.synced_folder "/Users/pyk/github.com", "/home/vagrant/go/src/github.com", type: "nfs"
  end
end
