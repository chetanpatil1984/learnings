### Environment

Fedora linux 30

### Installation of VirtualBox and Vagrant

+ [VirtualBox download](https://www.virtualbox.org/wiki/Downloads)  
`sudo dnf localinstall VirtualBox-6.0-6.0.10_132072_fedora29-1.x86_64.rpm`  
*\*Also install the extension pack if required*  

+ [Vagrant download](https://www.vagrantup.com/downloads.html)  
`sudo dnf localinstall vagrant_2.2.5_x86_64.rpm`  

### Example usage
```bash
vagrant -v
mkdir vagrant-workspace/generic-oracle8
cd vagrant-workspace/generic-oracle8
vagrant init generic/oracle8
# VM configuration done via Vagrantfile.
cat Vagrantfile
# Should run from folder where vagrant init was invoked from.
# Saves current state of VM.
vagrant suspend 
# Destroys current state of VM. It is like shutdown.
vagrant halt
vagrant resume
vagrant up 
vagrant status
vagrant ssh
```

### Vagrantfile configuration examples

```
# Create host-only network adapter
  config.vm.provider "virtualbox" do |vb|
      config.vm.network "private_network", :type => 'dhcp', :adapter => 2
  end
```
