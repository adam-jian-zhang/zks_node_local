# ZKS_NODE_LOCAL

Ansible scripts to setup ZKS nodes, the playbook will run based on the roles of the node, and
in priciple it should only touch itself.

## Usage

```bash
ansible-playbook --private-key {{ ansible deploy key }} -u {{ ansible user }} -i inventory.ini site.yaml -vvv

# node agent
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini node_agent.yml -vvv

# gpu-operator
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini gpu-operator.yml -e "@extra-vars.yml" -vvv

# cuda
ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini cuda.yml -e "@extra-vars.yml" -vvv

ansible-playbook --private-key ~/.ssh/id_ed25519 -i inventory.ini images.yml
```

### docker

```bash
# docker
ansible-playbook --private-key ~/.ssh/id_ed25519 -u adamz -i inventory.ini docker.yml -vvv
```
### Golang

```bash
ansible-playbook --private-key ~/.ssh/id_ed25519 -u zhangjian -i inventory.ini golang.yml -vvv
```

### Erlang

```bash
ansible-playbook --private-key ~/.ssh/id_ed25519 -u zhangjian -i inventory.ini erlang.yml -vvv
```

### Desktop
```bash
ansible-playbook --private-key ~/.ssh/id_ed25519 -u zhangjian -i inventory.ini desktop.yml -vvv
```

### tools

```bash
ansible-playbook --private-key ~/.ssh/id_ed25519 -u adamz -i inventory.ini dev_tools.yml -vvv

ansible-playbook --private-key ~/.ssh/id_ed25519 -u adamz -i inventory.ini tkgi_toolkit.yml -vvv

ansible-playbook --private-key ~/.ssh/id_ed25519 -u adamz -i inventory.ini worker.yml -vvv
```

### NATS

```bash
ansible-playbook --private-key ~/.ssh/id_ed25519 -u zhangjian -i inventory.ini nats.yml -vvv
```