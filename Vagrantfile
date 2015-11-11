# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure('2') do |config|
  config.vm.provision 'shell', inline: 'echo Ansible Consul POC'

  config.vm.define 'consulBootstrap1' do |consulBootstrap1|
    consulBootstrap1.vm.box = 'ubuntu/trusty64'
    consulBootstrap1.vm.box_url = '.'
    consulBootstrap1.vm.hostname = 'consulBootstrap1'
    consulBootstrap1.vm.network 'public_network', bridge: "eth1"
    consulBootstrap1.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulBootstrap2' do |consulBootstrap2|
    consulBootstrap2.vm.box = 'ubuntu/trusty64'
    consulBootstrap2.vm.box_url = '.'
    consulBootstrap2.vm.hostname = 'consulBootstrap2'
      consulBootstrap2.vm.network 'public_network', bridge: "eth1"
    consulBootstrap2.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulServer1' do |consulServer1|
    consulServer1.vm.box = 'ubuntu/trusty64'
    consulServer1.vm.box_url = '.'
    consulServer1.vm.hostname = 'consulServer1'
    consulServer1.vm.network 'public_network', bridge: "eth1"
    consulServer1.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulServer2' do |consulServer2|
    consulServer2.vm.box = 'ubuntu/trusty64'
    consulServer2.vm.box_url = '.'
    consulServer2.vm.hostname = 'consulServer2'
    consulServer2.vm.network 'public_network', bridge: "eth1"
    consulServer2.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulServer3' do |consulServer3|
    consulServer3.vm.box = 'ubuntu/trusty64'
    consulServer3.vm.box_url = '.'
    consulServer3.vm.hostname = 'consulServer3'
    consulServer3.vm.network "public_network", bridge: "eth1"
    consulServer3.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulClient1' do |consulClient1|
    consulClient1.vm.box = 'ubuntu/trusty64'
    consulClient1.vm.box_url = '.'
    consulClient1.vm.hostname = 'consulClient1'
    consulClient1.vm.network 'public_network', bridge: "eth1"
    consulClient1.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end

  config.vm.define 'consulClient2' do |consulClient2|
    consulClient2.vm.box = 'ubuntu/trusty64'
    consulClient2.vm.box_url = '.'
    consulClient2.vm.hostname = 'consulClient2'
    consulClient2.vm.network 'public_network', bridge: "eth1"
    consulClient2.vm.provider 'virtualbox' do |vb|
      # vb.gui = true
      vb.memory = '512'
      vb.cpus = 1
    end
  end
end
