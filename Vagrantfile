# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "jessie" do |jessie|
    jessie.vm.box = "debian/jessie64"
    jessie.vm.hostname = "ss"
    jessie.vm.network "private_network", ip: "192.168.33.10"

    jessie.vm.provider :virtualbox do |vb|
      vb.gui = false
      vb.memory = 512
      vb.cpus = 1
    end

    jessie.vm.synced_folder "/home/pyk/go", "/home/vagrant/go", type: "nfs"
  end
end
