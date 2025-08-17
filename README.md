# Setting up a home router on Debian with the help of Ansible

edit roles/freeradius/files/clients.conf
supply your own files in roles/freeradius/files/
	ca.pem (certificate authority, certifiate)
	server.pem (freeradius, certificate)
	server.key (freeradius, private key)

make sure you have ssh key for root user

execute like this:
1. connect future WAN interface to your existing LAN
2. `$ ansible-playbook primary.yml --user root`
3. now connect to real WAN
4. `$ ansible-playbook secondary.yml --user root`
