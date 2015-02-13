# ruthanet_deploy
rutha.net staging and deployment vagrant environment

## Install rutha.net
1. `git clone https://github.com/molekilla/rutha.net` into host machine
2. Share folder with guest machine

```ruby
  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "~/Code/rutha.net", "/home/vagrant/repos/rutha.net"
```

3. Provision VM

## Installation and provisioning (tested with Ubuntu trusty)
1. Install [Ansible](http://docs.ansible.com/intro_installation.html#getting-ansible)
2. Install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
3. Install [Vagrant](https://docs.vagrantup.com/v2/getting-started/)
4. `git clone https://github.com/molekilla/ruthanet_deploy`
5. `cd ruthanet_deploy`
6. Run `vagrant up`
7. Enjoy!
