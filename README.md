Ansible AWS Windows
===================

Uses Ansible to launch a Windows AMI in AWS and configure it to allow
management by Ansible over WinRM.

The second role configures a web application called ping.

```
ansible-playbook ssh_win_access.yml -i 52.14.180.52,18.117.186.244, -e ansible_user=Administrator -e ansible_pass=Praveen@1234
```
