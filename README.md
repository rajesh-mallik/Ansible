# Ansible
sudo su -
apt install ansible -y

mkdir /etc/ansible   # make directory
cd /etc/ansible       # go to derectoey

ansible-config init --disabled -t all > ansible.cfg
ls
ansible --version
vi hosts #create hosts file
sed -i 's;host_key_checking=True;host_key_checking=False;g' ansible.cfg
vi ansible.pem  #create pem file
chmod 400 ansible.pem 
ansible -m ping [webservers]

#filename (ansible.pem)
copy the private password and past

#write this command in hosts file
[webservers:vars]
ansible_ssh_user="ubuntu"
#ansible_ssh_password="password"
ansible_ssh_private_key_file="/etc/ansible/ansible.pem"
ansible_ssh_port=22
