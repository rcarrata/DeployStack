# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://vagrantcloud.com/nrel/CentOS-6.5-x86_64/version/4/provider/virtualbox.box"

  config.vm.define "controller" do |controller|
    controller.vm.network :private_network, ip: "192.168.11.3"
    controller.vm.network :private_network, ip: "192.168.22.3"
    controller.vm.hostname = "controller"
    # Otherwise using VirtualBox
    controller.vm.provider :virtualbox do |vbox|
      # Defaults
      vbox.customize ["modifyvm", :id, "--memory",
        1024]
      vbox.customize ["modifyvm", :id, "--cpus", 1]
  end
 end

end