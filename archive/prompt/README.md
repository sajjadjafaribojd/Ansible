# Ansible Playbook with Multiple Prompts

This Ansible playbook demonstrates how to use multiple prompts to gather user input during playbook execution.

## Prerequisites

- Ansible installed on your local machine.
- MySQL server running on the target host (localhost in this case).
- Necessary MySQL Python libraries installed on the control machine.

## Usage

Run the playbook and provide the necessary inputs when prompted:

```sh
ansible-playbook playbook.yml

# Explanation

## Prompts

The playbook uses `vars_prompt` to ask the user for the `db_user` and `db_password`. The `private: yes` option for `db_password` ensures that the password input is not displayed on the screen, enhancing security.

## Tasks

The playbook contains a single task:

- **Create a database user**: This task creates a new MySQL user with the username and password provided by the user. It grants the new user all privileges on all databases.

## Security Note

- The password is prompted with `private: yes` to prevent it from being displayed.
- Ensure your playbook and any sensitive data are stored securely and not exposed in version control.

# License

This project is licensed under the MIT License.
