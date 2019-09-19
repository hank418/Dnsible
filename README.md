# Dnsible
Dennis Ansible Project

## Initial
#### Add config & inventory file
```shell
$ cp ansible.cfg.example ansible.cfg
$ cp inventories/hosts.example inventories/hosts
```
#### Modify your remote node username & private key
ansible.cfg
```
[defaults]

inventory = inventories/hosts
remote_user = ansible
private_key_file = ~/.ssh/id_rsa
retry_files_save_path = ./ansible-retry
callback_whitelist = profile_tasks
```
#### Define your remote node ip
inventories/hosts
```
[demo_group]
demo1 ansible_ssh_host=256.256.256.256
```