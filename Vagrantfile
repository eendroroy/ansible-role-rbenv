# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
  	vb.gui = false
  	vb.memory = 256
  end

  config.vbguest.auto_update = false

  config.vm.define 'trusty' do |trusty|
    trusty.vm.box = "ubuntu/trusty64"
    trusty.vm.box_check_update = false
    trusty.vm.network "private_network", ip: "192.168.33.11"
  end

  config.vm.define 'xenial' do |xenial|
    xenial.vm.box = "ubuntu/xenial64"
    xenial.vm.box_check_update = false
    xenial.vm.network "private_network", ip: "192.168.33.12"
  end

  config.vm.define 'centos7' do |centos7|
    centos7.vm.box = "centos/7"
    centos7.vm.box_check_update = false
    centos7.vm.network "private_network", ip: "192.168.33.14"
  end
end
