# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "sagarpatke/bullseye64-lightdm-mate"

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    vb.gui = true
  
    # Customize the amount of memory on the VM:
    vb.cpus = 2
    vb.memory = "4069"

    vb.customize ["modifyvm", :id, "--vram", "256"]
  end
  
  config.vm.provision :shell, inline: "apt-get update && apt-get install -y thunderbird"
end

