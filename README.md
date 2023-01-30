# ansible-playbooks
collection of ansible tasks and playbooks

This will be a place to share some of my playbooks I use at my daily it engineer.

<h2>00-user-create.yml</h2>

This script will help you to deploy your user fast and easy without the need to copy the SSH key or create the user

<h5>Variables:</h5>
Ansible Playbook Hostnames out of your inventory
hosts: <hostname>

Your SSH user you want to create
SSH_USER: <os-username>

The user id you want to set for the user
SSH_USER_UID: <os-id>

The group the user will be joined (sudo is for Ubuntu perfect)
SSH_USER_GROUP: sudo

Your GitHub Username to receive your public SSH Key
GITHUB_USERNAME: <github username>

<h5>Use the Playbook:</h5>

To use the Playbook with Username and Passwort to setup your SSH Key User use the following Command:
-b will use sudo for this playbook
-K asks you before the play for your sudo password (not need if you use root)

<code>ansible-playbook 00-user-create.yml -b -K</code>

