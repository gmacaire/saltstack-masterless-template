# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vbguest.auto_update = true

  config.vbguest.no_remote = false

  config.vm.box = "ubuntu_1210"

  config.vm.box_url = "http://cloud.github.com/downloads/roderik/VagrantQuantal64Box/quantal64.box"

  config.vm.hostname = "ssmt-vm"

  config.vm.network :private_network, ip: "192.168.33.123"

  config.vm.provision :salt do |salt|

    salt.install_args = "v0.14.1"

    salt.install_type = "git"

    salt.minion_config = "etc/salt/minion"

    salt.run_highstate = true

    salt.verbose = true

  end

  config.vm.synced_folder "/local/path/to/project/etc/salt/srv", "/srv/salt"

end