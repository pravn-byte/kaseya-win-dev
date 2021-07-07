Ansible AWS Windows
===================

Uses Ansible to launch a Windows AMI in AWS and configure it to allow
management by Ansible over WinRM.

The second role configures a web application called ping.

```
ansible-playbook -i hosts aws-windows.yml. 
```
