# COYO Ansible Playbook

## TL;DR

```
ansible-playbook --connection=local --inventory 127.0.0.1 playbook.yml --extra-vars "coyo_version=18.11.5 coyo_url=contoso.com coyo_profile=prod coyo_management_user=admin coyo_management_password=coyo4admin coyo_db_name=coyo coyo_db_user=coyo-postgres coyo_db_password=Sup3rD4tabase"
```

## Introduction

This playbook makes it really easy to install COYO on a new Ubuntu host.

## Requirements

- Ubuntu 18.04 LTS
- Python ```apt install python```
- pyOpenSSL ```apt install python-openssl```
- Ansible ```apt install ansible```
- unzip binary ```apt install unzip```
- sudo ```apt install sudo```

## Install COYO

To install COYO, you need to clone this repository first and then run the Ansible Playbook on your local Ubuntu host. 

```
apt install python python-openssl ansible unzip sudo

git clone https://github.com/DasLeo/coyo-ansible.git
cd coyo-ansible

ansible-playbook --connection=local --inventory 127.0.0.1 playbook.yml --extra-vars "coyo_version=18.11.5 coyo_url=contoso.com coyo_profile=prod coyo_management_user=admin coyo_management_password=coyo4admin coyo_db_name=coyo coyo_db_user=coyo-postgres coyo_db_password=Sup3rD4tabase"
```
