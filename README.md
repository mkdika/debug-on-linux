# Debug on Linux

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](/LICENSE)

Docs, references, notes, tip & tricks, and supporting tools for Debugging on Linux.


## Vagrant & Environment Provision

The vagrant vm template to ease tool & utilities provision.

### Requirement

- [Install VirtualBox](https://www.virtualbox.org/wiki/Downloads), I use VirtualBox 6.0
- [Install Vagrant](https://www.vagrantup.com/docs/installation/), I use Vagrant 2.2
- [Install Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html), I use Ansible 2.8

### Running

```bash
# To create, start and provision Vagrant for the first time
vagrant up

# To re-provision Vagrant (need to 'vagrant up' beforehand)
vagrant provision

# To remote (ssh) inside Vagrant
vagrant ssh

# To stop Vagrant
vagrant halt

# To check Vagrant status
vagrant status

# To destroy (remove) Vagrant
vagrant destroy
```

### Customization

- __Hardware specs__

  Vagrant vm specs by default is:
  - CPUs: 2
  - Memory: 2GB
  - Storage: 10GB

  You can customize it by set the environment variable in host OS, as:
  - `VAGRANT_CPUS`, for number of CPUs. eg. `VAGRANT_CPUS=4`
  - `VAGRANT_MEMORY`, for number of memory in MB. eg. `VAGRANT_MEMORY=4096`
  - `VAGRANT_STORAGE`, for number of storage. eg. `VAGRANT_STORAGE=20GB`

  You will need to pre-install Vagrant's disksize plugin in order to ease the storage size customization.
  To install the plugin, run:

  ```bash
  vagrant plugin install vagrant-disksize
  ```

  Destroy and re-up Vagrant if been exists.



## License

License under the MIT license. See [LICENSE](/LICENSE) file.
