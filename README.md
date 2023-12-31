# Ansible Collection - my0373.laptop

This is a collection of roles I use to help me configure Fedora.

# Versions
These roles are currently tested for Fedora 38, and 39 beta
# Using the collection
Example playbooks for each of the following roles is available [here](https://gitlab.com/my0373-ansible/playbooks/ansible-fedora-laptop).

# Included roles
The current roles included are...

## chrome
Install and configure Google Chrome
## fonts
Install and configure a set of standard fonts
## git
A role to install and configure git for a local user on the target system.

parameters
# Parameters for the git role


### The git plaintext username
    GIT_USER: "Matt York"
### The git email address to use
    GIT_EMAIL: "my0373@gmail.com"
### The default editor 
    GIT_EDITOR: "vim"
### Git will autosetup the remote branch.
    GIT_AutoSetupRemote: "true"
### Git push default
    GIT_PUSH_DEFAULT: "simple"

## kvm
Install and configure the linux KVM hypervisor.

## motd
Install a simple message of the day

## osupdate
A simple role to update the OS

## packer
Install and configure Hashicorp Packer.

## rpmfusion
Add the rpmfusion repositories

## system_roles
Install the linux system roles collection.

## terraform
Configure the Hashicorp Terraform repositories.

## tmux
Install and configure the TMUX terminal manager.

## vim
Install and configure vim with a configuration for Ansible and YAML files.

## vscode
Install the VSCode application, repositories and configuration.

## zsh
Install and configure the ZSH with omzsh

# Installing the collection


This collection can be installed directly 
### Install the collection from the from the command line.

```
$ ansible-galaxy collection install  git+https://gitlab.com/my0373/ansible-my0373-fedora.git
```

or 
### Install the collection from a ```requirements.yml``` file

Firstly, create a file called ``` requirements.yml ``` with the following content.

```
collections:
  - name: https://gitlab.com/my0373-ansible/collections/my0373/ansible-my0373-fedora.git
    type: git
    version: main
```

You can then install the collection using the command

```
$ ansible-galaxy install -r requirements.txt
```

This will install the latest version of the collection from the ```main``` branch.


# Work in progress
Some key things that need to be added

* selinux enforcing
* firewall enforcing
* chrony installed and configured to use ntp servers
* install a few of my favourite tools (tree, vim-enhanced, htop, netcat)