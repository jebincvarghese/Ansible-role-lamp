# Ansible-role-lamp


## STACK


- Apache Webserver
- php7.4
- Mariadb-database-server


## Prerequisites


- Latest ansible version installed.


## Hosts


- Add hosts in an inventory file(say hosts) under your working directory.


## Configuration

- Configuration of variables for both apache mariadb(domain_name,mariadb_root_password,database_name,database_username,database_user_password) are included in the main.yml file the vars section, which can be modified as per the requirement.

## Setup

To check if the playbook have any syntax error, run:
```
ansible-playbook -i inventory_file wordpress.yml --syntax-check
```

## Running playbook

```
ansible-playbook -i inventory_file wordpress.yml 
```

Once the above steps has been completed, your wordpress will be ready in the specified domain name.


