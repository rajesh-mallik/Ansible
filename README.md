# Ansible

mkdir /etc/ansible   # make directory
cd /etc/ansible       # go to derectoey

ansible-config init --disabled -t all > ansible.cfg
ls
ansible --version
vi hosts #create hosts file
sed -i 's;host_key_checking=True;host_key_checking=False;g' ansible.cfg
vi ansible.pem  #create pem file
chmod 400 ansible.pem 
ansible -m ping [webserver]
