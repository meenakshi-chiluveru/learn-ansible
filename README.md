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
