# Ansible Collection - my0373.laptop

This is a little collection of roles I use to configure Fedora
Some key things that need to be added

* selinux enforcing
* firewall enforcing
* chrony installed and configured to use ntp servers
* install a few of my favourite tools (tree, vim-enhanced, htop, netcat)

This collection can be installed directly 
### Install the collection from the from the command line.

```
$ ansible-galaxy collection install  git+https://gitlab.com/my0373/ansible-my0373-fedora.git
```

or 
### Install the collection from a requirements.yml file

Firstly, create a file called ``` requirements.yml ``` with the following content.

```
collections:
  - name: https://gitlab.com/my0373-ansible/collections/my0373/ansible-my0373-fedora.git
    type: git
    version: main
```

You can then install the collection using the command

```
ansible-galaxy install -r requirements.txt
```

This will install the latest version of the collection from the ```main``` branch.