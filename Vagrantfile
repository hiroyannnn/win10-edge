# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "win10-edge"
  # config.vm.box = "Microsoft/EdgeOnWindows10"
  config.vm.guest = :windows
  config.vm.communicator = "winrm"
  config.vm.network :forwarded_port, guest: 3389, host: 13389
  config.vm.network :forwarded_port, guest: 5985, host: 15985, id: "winrm", auto_correct: true

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.customize ["modifyvm", :id, "--paravirtprovider", "hyperv"]
  end
end
