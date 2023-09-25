# dev_tools

Ansible scripts to setup dev environment.

## Usage

```bash
ansible-playbook --private-key {{ ansible deploy key }} -u {{ ansible user }} -i inventory.ini site.yaml -vvv

# node agent
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini node_agent.yml -vvv
```

