# Ansible Playbook with Tags

This playbook demonstrates how to use tags in Ansible to selectively run specific tasks.

## Running the Playbook with Tags

You can run the playbook with specific tags using the `--tags` option. Here are a few examples:

### Run only the installation tasks:

```sh
ansible-playbook playbook.yml --tags "install"
