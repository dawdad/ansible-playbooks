# ansible-playbooks
collection of ansible tasks and playbooks

This will be a place to share some of my playbooks I use at my daily.

<h2>00-user-create.yml</h2>

This script will help you to deploy your user fast and easy without the need to copy the SSH key or create the user

<h3>Variables:</h3>

Ansible Playbook Hostnames out of your inventory
<code>hosts: hostname</code>

Your SSH user you want to create
<code>SSH_USER: os-username</code>

The user id you want to set for the user
<code>SSH_USER_UID: os-id</code>

The group the user will be joined (sudo is for Ubuntu perfect)
<code>SSH_USER_GROUP: sudo</code>

Change the value to a passwort you wish for the user (This is needed for sudo -i command)
<code>password</code>

Your GitHub Username to receive your public SSH Key
<code>GITHUB_USERNAME: github username</code>

<h3>Use the Playbook:</h3>

To use the Playbook with Username and Passwort to setup your SSH Key User use the following Command:
-b will use sudo for this playbook
-K asks you before the play for your sudo password (not need if you use root)

<code>ansible-playbook 00-user-create.yml -b -K</code>

