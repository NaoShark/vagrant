# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-18.04"

  config.vm.define "openstack" do |openstack|
    openstack.vm.network "private_network", ip: "192.168.33.10"

    openstack.vm.provider "virtualbox" do |vb|
      vb.memory = "4096"
    end
  end

  config.vm.define "minio" do |minio|
    minio.vm.network "private_network", ip: "192.168.33.20"

    minio.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
    end
  end

  config.ssh.forward_agent = true

end
