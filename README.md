# ruthanet_deploy
rutha.net staging and deployment vagrant environment

## Installation (tested with Ubuntu trusty)
1. Install [Ansible](http://docs.ansible.com/intro_installation.html#getting-ansible)
2. Install [Virtualbox](https://www.virtualbox.org/wiki/Downloads)
3. Install [Vagrant](https://docs.vagrantup.com/v2/getting-started/)
4. git clone https://github.com/molekilla/ruthanet_deploy
5. cd ruthanet_deploy
6. Run `vagrant up`
7. Enjoy!

## To start developing ASP.NET (beta 1 or 2)
1. Run `vagrant ssh`
2. Run `curl -sSL https://raw.githubusercontent.com/aspnet/Home/master/kvminstall.sh | sh && source ~/.kre/kvm/kvm.sh`
3. Install latest kpm with `kvm upgrade`
4. Run apps with `k kestrel`
