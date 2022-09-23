# Infra

Automatic infrastructure for my home.

## Usage

Clone the repository on your Ansible [control node.](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#control-node-requirements):

```
git clone https://github.com/jokocide/iac
```

Verify that the community.general collection is available.

```
ansible-galaxy collection list
```

If it is not, install it.

```
ansible-galaxy collection install community.general
```

The repository contains files with names in the format of "subject_example.yml" and should be replaced with files that are named identically, but without the example.

For example, hosts_example.yml should be hosts.yml. The example files contain data that can be copied over and modified.

After creating the required files, the run.yml playbook can be used.

```
ansible-playbook run.yml -K -e "@vars/private.yml"
```
