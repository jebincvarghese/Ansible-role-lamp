# ansible-role-lamp

A basic LAMP stack environment that creates an environment for wordpress websites which is built using ansible roles. It consists of the following:

- Apache Webserver
- PHP 7.4
- MariaDB server
- Wordpress (latest)

## Prerequisites

- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- Ansible-galaxy
- SSH and key-based authentication from the ansible machine to the remote server.

## Variables Used

```
mariadbroot_pw: "mysqlpass123" #-------database root password-------#
wp_username: wordpress
wp_password: wordpress
wp_database: wordpress

```

## Features

In this demo, we will be making use of 2 ansible roles - LAMP & WordPress. 
- LAMP : In lamp role, we will be installing and configuring Apache, MySQL, PHP and its required dependencies.
- WordPress : In wordpress role, we will downloading the latest wordpress, extracting its contents and setting up the custom wp-config.php file to complete its installation.

## Usage

1. Initially, create 2 roles - lamp & wordpress in the roles_path using the below command
```
ansible-galaxy init lamp
ansible-galaxy init wordpress
```
2. Get the contents of the roles - lamp & wordpress and place them in location 'roles_path' specified in the ansible config file (ansible.cfg).

3. Then, you can run the main.yml playbook using the command
```
ansible-playbook -i inventory main.yml
```

Once the above steps has been completed, your wordpress will be ready in the specified domain name.


## Result


