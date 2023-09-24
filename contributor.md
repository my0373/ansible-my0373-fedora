# Building
## Building the collection locally for testing
### Prequsites
* A Fedora host
* Ansible-galaxy
* Ansible-builder

### Installing the collection

#### From a requirements file

    ---
    collections:
      - name: https://github.com/my0373/ansible-my0373-fedora.git
        type: git
        version: main

#### Install the collection from the local file.
    ansible-galaxy collection install -r [path to requirements.yml]

#### If you need to, you can delete the local collections. By default, they are found here

    rm -rf ~/.ansible/collections/ansible_collections/my0373
