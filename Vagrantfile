# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define :lb1 do |lb1|
    lb1.vm.box = "precise-server-cloudimg-amd64-vagrant"
    lb1.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-amd64-vagrant-disk1.box"
    lb1.vm.network :private_network, ip:  "192.168.99.10"
    lb1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "256"]
    end
  end
  config.vm.define :web1 do |web1|
    web1.vm.box = "raring-server-cloudimg-amd64-vagrant"
    web1.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/raring/current/raring-server-cloudimg-amd64-vagrant-disk1.box"
    web1.vm.network :private_network, ip:  "192.168.99.12"
    web1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "256"]
    end
  end
  config.vm.define :web2 do |web2|
    web2.vm.box = "raring-server-cloudimg-amd64-vagrant"
    web2.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/raring/current/raring-server-cloudimg-amd64-vagrant-disk1.box"
    web2.vm.network :private_network, ip:  "192.168.99.13"
    web2.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "256"]
    end
  end
  config.vm.define :db1 do |db1|
    db1.vm.box = "precise-server-cloudimg-amd64-vagrant"
    db1.vm.box_url = "http://cloud-images.ubuntu.com/vagrant/precise/current/precise-server-cloudimg-amd64-vagrant-disk1.box"
    db1.vm.network :private_network, ip:  "192.168.99.15"
    db1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "256"]
    end
  end
end
