# ansible
### First Installation
**create inventory file**
Add the ips of the computers you want to manage
```
~: nano inventory
192.168.4.1
```

**Test Ansible is working**
```
 ansible all --key-file ~/.ssh/ansible -i inventory -m ping
```


**Create ansible config file**
```
 ~: nano ansible.cfg
 
 [defaults]
 inventory = inventory
 private_key_file = ~/.ssh/ansible
```


**Now the ansible command can be simplified**
```
 ansible all -m ping
```


**List all of the hosts in the inventory**
```
 ansible all --list-hosts
```


**Gather facts about your hosts**
```
 ansible all -m gather_facts
```


**Gather facts about your hosts, but limit it to just one host**
```
 ansible all -m gather_facts --limit 172.16.250.132
```
