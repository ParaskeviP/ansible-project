## Run Ansible with Vagrant

Start all vms by running in terminal to the directory where VagrantFile is located:

```bash
vagrant up
```

Add the ssh config
```bash
ssh-config >> ~/.ssh/config
```

Go to the directory where ansible.cfg is located and run all the playbooks

 - for database playbook
```bash
ansible-playbook -l dbserver-vm playbooks/postgres.yaml
```

 - for Springboot playbook
```bash
ansible-playbook -l appserver-vm playbooks/spring.yaml
```

- for Frontserver playbook
```bash
ansible-playbook -l frontend-vm playbooks/vuejs.yaml
```

You can see the project by typing the ip http://192.168.56.103 in a browser.


## Run Docker and Ansible 

Start all vms by running in terminal to the directory where VagrantFile is located:

```bash
vagrant up docker
```

Add the ssh config
```bash
ssh-config >> ~/.ssh/config
```

Go to the directory where ansible.cfg is located and run 
```bash
ansible-playbook -l docker-vm playbooks/spring-vue-docker.yml
```

You can see the project by typing the ip http://192.168.56.104 in a browser.


## Run Kubernets with Ansible

Go to the directory where ansible.cfg is located and run this in terminal

```bash
ansible-playbook -l k8s-vm playbooks/k8s.yaml
```

Type in your browser http://ylision.ddns.net/ to see project.