## Base repo
En esta carpeta, organizamos toda nuestra infraestructura

# tests:
ansible  demo -m ping -i inventories/server.yaml
ansible  all -m ping -i inventories/server.yaml

# Playbooks
ansible-playbook -i inventories/server.yml playbooks/playbook-base-linux.yml
