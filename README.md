Vagrant + Ansible example
-------------------------

This is an example of how to use Vagrant together with Ansible, based on
my own playbooks. It has been released in this form in response to a
[post on ansible-project](https://groups.google.com/forum/#!topic/ansible-project/Dk6yyrW8s9E)
about using Vagrant and Ansible together.

Usage
-----

Make sure to have Vagrant's ssh key loaded, then:

* `ansible-playbook --inventory-file hosts.ini vagrant-setup.yml`
* Optionally followed by `ansible-playbook --inventory-file hosts.ini --ask-sudo-pass add-vagrant-hostnames-to-etc-hosts.yml`

This will add the vagrant public key to the root user so you can connect directly as root using the vagrant ssh key, update apt so package installs don't fail because of outdated metadata, and manage */etc/hosts* on the VM's so they can refer to each other by name.

If you ran the second playbook as well, which is optional, it will also add those same names to your local */etc/hosts*, in the form of *hostname*.vagrant

License
-------

Released into the public domain, please feel free to use these however you see fit :)