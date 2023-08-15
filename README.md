# ansible-playbooks
collection of ansible tasks and playbooks

This will be a place to share some of my playbooks I use at my daily.

<h2>00-user-create.yml</h2>

This script will help you to deploy your user fast and easy without the need to copy the SSH key or create the user

Copy the all.yml.example to all.yml

You need to change the Variables in the all.yml file in the group_all folder:
<h3>Variables:</h3>

Ansible Playbook Hostnames out of your ansible inventory
<code>ANSIBLE_HOSTS: hostname</code>

Your SSH user you want to create
<code>SSH_USER: os-username</code>

The user id you want to set for the user
<code>SSH_USER_UID: os-id</code>

The group the user will be joined (sudo is for Ubuntu perfect)
<code>SSH_USER_GROUP: sudo</code>

Change the value to a passwort you wish for the user (This is needed for sudo -i command) - Need to change the <PASSWORD> in the string.
<code>SSH_USER_PASSWORD</code>

Your GitHub Username to receive your public SSH Key
<code>GITHUB_USERNAME: github username</code>

The comment which will be showen in the /etc/passwd file behind the user (Optional)
<code>ANSIBLE_COMMENT</code>

<h3>Use the Playbook:</h3>

To use the Playbook with Username and Passwort to setup your SSH Key User use the following Command:
-K asks you before the play for your sudo password (not need if you use root)

<code>ansible-playbook 00-user-create.yml -b -K</code>

With dedicated ansible inventory

<code>ansible-playbook 00-user-create.yml -K -i ~/.ansible/hosts</code>

