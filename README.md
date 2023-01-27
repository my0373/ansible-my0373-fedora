# Ansible Collection - my0373.laptop

This is a little collection of roles I use to configure Fedora
Some key things that need to be added

* selinux enforcing
* firewall enforcing
* chrony installed and configured to use ntp servers
* install a few of my favourite tools (tree, vim-enhanced, htop, netcat)

This collection can be installed with
    ansible-galaxy collection install  git+https://gitlab.com/my0373/ansible-my0373-fedora.git
