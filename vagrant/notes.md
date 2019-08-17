### Environment

Fedora linux 30

### Installation of VirtualBox and Vagrant

[VirtualBox download](https://www.virtualbox.org/wiki/Downloads)
`sudo dnf localinstall VirtualBox-6.0-6.0.10_132072_fedora29-1.x86_64.rpm`
| Also install the extension pack if required

[Vagrant download](https://www.vagrantup.com/downloads.html)
`sudo dnf localinstall vagrant_2.2.5_x86_64.rpm`

### Example usage
```
vagrant -v
mkdir vagrant-workspace/generic-oracle8
cd vagrant-workspace/generic-oracle8
cat Vagrantfile
vagrant init generic/oracle8
# Should run from folder where vagrant init was invoked from.
# saves current state of vm
vagrant suspend 
# destroys current state of vm. It is like shutdown.
vagrant halt 
vagrant up 
vagrant status
vagrant ssh
```
