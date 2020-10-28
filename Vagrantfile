# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "docker" do |docker|
      docker.vm.provider :virtualbox do |vb|
        vb.name = "linuxdocker"
      end
      docker.vm.box = "alpine/alpine64"
      docker.vm.provision "shell", path: "script.sh"
      docker.vm.network "forwarded_port", guest: 80, host: 8009
      docker.vm.synced_folder "D:/ClasesUnivalle/SO/vagrant/vagrantdockeralpine/www/", "/home/estudiante"
  end
end