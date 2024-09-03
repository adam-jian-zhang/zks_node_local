# TKGN_NODE_LOCAL

Ansible scripts to setup TKGN nodes, the playbook will run based on the roles of the node, and
in priciple it should only touch itself.

## Usage

```bash
ansible-playbook --private-key {{ ansible deploy key }} -u {{ ansible user }} -i inventory.ini site.yaml -vvv

# node agent
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini node_agent.yml -vvv

# dev_tools
ansible-playbook --private-key ~/.ssh/id_ed25519 -u zhangjian -e user=zhangjian  -i inventory.ini dev_tools.yml -vvv

# gpu-operator
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini gpu-operator.yml -e "@extra-vars.yml" -vvv

# cuda
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini cuda.yml -e "@extra-vars.yml" -vvv

ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini images.yml
```

