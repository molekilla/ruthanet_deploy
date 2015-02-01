# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version.
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu/trusty64"

  # The url from where the 'config.vm.box' box will be fetched if it
  # doesn't already exist on the user's system.
  config.vm.box_url = "https://atlas.hashicorp.com/ubuntu/boxes/trusty64/versions/14.04/providers/virtualbox.box"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  config.vm.network :private_network, ip: "192.168.88.88"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Configure VirtualBox.
  config.vm.provider :virtualbox do |vb|
    # Set the RAM for this VM to 512M.
    vb.customize ["modifyvm", :id, "--memory", "512"]
  end

  config.ssh.forward_agent = true

  # Enable provisioning with Ansible.
  config.vm.provision "ansible" do |ansible|
#    ansible.groups = {
#        "aws" => ["default"]
#    }      
#    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    ansible.playbook = "provisioning/playbook.yml"
    ansible.verbose = 'v'
    ansible.sudo = true
  end
end