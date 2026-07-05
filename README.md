# ansible-project-2026

ansible installation in ANSIBLE TOWER
sudo dnf update -y

sudo dnf install ansible-core -y


NGINX installation in APP-SERVER
sudo dnf install nginx -y

sudo systemctl enable nginx

sudo systemctl start nginx


ansible all -i inventory/prod.yaml -m ping
ansible-playbook -i inventory/prod.yaml paybooks/stop-nginx.yml
ansible-playbook -i inventory/prod.yaml paybooks/start-nginx.yml



To Setup Connection between Ansible Tower and Ansible target host:
Copy the public key for different ec2 instance(Ansible target host) to ansible-tower
Then add Ansible target host public key to  ~/.ssh/ location

Here May_2026.pem is the public key of Ansible target host
Steps: 
cp May_2026.pem ~/.ssh/

chmod 400 ~/.ssh/May_2026.pem
