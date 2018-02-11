# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.define 'mstr' do |node|
    node.vm.hostname = 'mstr'
    node.vm.network "private_network", ip: '10.130.63.10'
  end

  (0..1).each do |i|
    hostname = "node#{i}"
    config.vm.define hostname do |node|
      node.vm.hostname = hostname
      node.vm.network "private_network", ip: "10.130.63.#{20 + i}"
    end
  end

end
