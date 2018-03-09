# Ansible

## Dependency
```sh
ansible-galaxy install AnsibleShipyard.ansible-zookeeper
```

## Ansible Env Config
See [here](http://docs.ansible.com/ansible/intro_installation.html) to install Ansible. After this, run the following command to confirm install successfully:
```sh
ansible --version
```

Lots of Ansible's config files are under `/etc/ansible`, usually non-editable, so for your convenience, run the following command under `/etc/ansible` to change access permission:
```sh
sudo chmod -R 777 /etc/ansible
```

To use Ansible Dynamic Inventory, you need to download the following files and put them under `/etc/ansible`:
* https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.ini
* https://raw.githubusercontent.com/ansible/ansible/devel/contrib/inventory/ec2.py

Run the following command to grant `ec2.py` script permission to run:
```sh
chmod +x /etc/ansible/ec2.py
```

To modify the default configuration of Ansible, please put the text below into `/etc/ansible/ansible.cfg`
```ini
inventory = /etc/ansible/ec2.py
host_key_checking = False
```