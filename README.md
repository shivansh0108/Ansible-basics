# Ansible-basics
Sample E-Commerce Website.

1. Create two machines with one as ansilbe server (master) and the second one as child node (slave) for that ansible server.  (I have used a Virtual Box setup by using Centos image and created the same )

2. Download the required packages (ansible package) on the server's (master and slave).

# yum install epel-release -y
# yum install ansible -y

3. After that create the playbooks as per your requirement. I have created two playbooks as mentioned below :-
Playbook 1 :- packages.yml (for installing required packages on the child node)
Playbook 2 :- fire.yml (for the firewalld configurations)
NOTE :- Playbooks may differ and you can create multiple playbooks or even create a single playbook according to your convenience)

4. After creatng the playbooks you can even test the same by executing following command on the master server :-

# ansible-playbook playbook.yml --check  (This will give you the status of all thee steps with success or failure )

5. Configure the database and the php connections on the slave server (CHILD NODE) according to your requirement. (In this case I have used a dummy e-commerce website which was available ove the internet for learning purpose)
