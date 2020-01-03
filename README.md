# ansible-training
repository for the Udemy course on Ansible

## ansible command
`ansible <hosts> -a <command>`
`ansible <hosts> -m <module>`

## establish a ping:
`ansible target1 -m ping -i inventory.txt`

```shell script
# Sample Inventory File

# Web Servers
web1 ansible_host=server1.company.com ansible_connection=ssh ansible_user=root ansible_ssh_pass=Password123!
web2 ansible_host=server2.company.com ansible_connection=ssh ansible_user=root ansible_ssh_pass=Password123!
web3 ansible_host=server3.company.com ansible_connection=ssh ansible_user=root ansible_ssh_pass=Password123!

# Database Servers (Windows)
db1 ansible_host=server4.company.com ansible_connection=winrm ansible_user=administrator ansible_password=Password123!

# Groups
[web_servers]
web1
web2
web3

[db_servers]
db1

# Groups of groups
[all_servers:children]
web_servers
db_servers
```
