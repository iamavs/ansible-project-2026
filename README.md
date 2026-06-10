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



To public key for different ec2 instance to ansible-tower
add their public key 

cp May_2026.pem ~/.ssh/

chmod 400 ~/.ssh/May_2026.pem
