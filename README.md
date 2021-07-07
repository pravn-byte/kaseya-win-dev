Ansible AWS Windows
===================

Uses Ansible to launch a Windows AMI in AWS and configure it to allow
management by Ansible over WinRM.

The second role configures a web application called ping.

```
ansible-playbook ssh_win_access.yml -i 52.14.180.52,18.117.186.244, -e ansible_user=Administrator -e ansible_pass=Praveen@1234
```

Run the job from Jenkins 
```
1. Login into Jenkins
2. Go to managed plugins and install ansible
3. Create new job with pipeline 
4. Select the build from SCM
5. Give url of this Repo
6. Save the job
8. Run the build with parameters
```
