# learn-ansible

install
``````
sudo pip-3.11 install ansible

`````````

ansible going to connect list of servers so ansible reqiures inventory file


create inventory file  - vim servers


connecting to node: create inventory file and node ip address in inventory file
command to connect remote server: ansible -i inventoryfilename all -e ansible-user=ansible -e ansible-password=DevOps321 -m ping


ansible is declarative
ansible supports heterogenous by default
ansible can scale to large infrastructure


how ansible conncts to node to push
ansible uses ssh


```````````````````````
how ansible manages node configuration
earlier = modules
latest collections
``````````````````````````
`````````
how ansible handles
install collection
file collection
service collection
ansible playbook
`````````````````````````
``````
ansible playbook will be written in YAML(yet another markup language) markup language
file extension can be like .yml or .yaml
inputs will be in the form of key:value pairs those will be plain or list or map/dictionary
a:10 - plain
a: [ 10,20 ]

``````````````````

`````````````````````
ansible is expecting the inputs in yaml
keys(parameters) are provoded by yaml
some values are provided by ansible

` ````````````````````````````
sample palybook
````
sample.yml
- name: some playbook
  hosts: all
  tasks:
   - name: demo task
     ansible.builtin.yum:
       name: nginx
       state: installed
- name: some role paly
  hosts: all
  roles:
    - demo

sample.yaml is playbook every playbook starts with a list meaning it can have one or more plays
-name keyword on play is optional and it is good to have
- host must to have keyword
-either tasks/roles is a msut to have role
---
`````
to run playbook
ansible -i ip address, all -e ansible_user=ec2-user -e ansible_password=DevOps321 -m ping
ansible-playbook -i 174.129.126.165, -e ansible-user=ec2-user -e ansible-password=DevOps321 01-demo.yaml

``````
