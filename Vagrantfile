# -*- mode: ruby -*-
# vi: set ft=ruby 


Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty32"

  # Mandelbrot/Poetry Server Port. You may need to adjust.
  config.vm.network "forwarded_port", guest: 7191, host: 7191

  # Synchronise Folders
  config.vm.synced_folder "./work", "/work"
  config.vm.synced_folder "./work", "/home/vagrant/work"

  config.vm.provision "shell", inline: <<-SHELL
    sudo locale-gen en_AU.UTF-8
    sudo apt-get update
    sudo apt-get -y install gcc build-essential gdb valgrind git
    echo "All done! Provisioning complete."
    echo "You can now connect by typing 'vagrant ssh'."
  SHELL
end
