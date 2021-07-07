// Build Parameters
properties([ parameters([
  string( name: 'WINDOWS_SERVER_ADMIN', defaultValue: 'Administrator'),
  string( name: 'WINDOWS_SERVER_PASS', defaultValue: 'Praveen@1234')
  string( name: 'WINDOWS_SERVER_IP', defaultValue: '52.14.180.52')
]), pipelineTriggers([]) ])

ansible_user = WINDOWS_SERVER_ADMIN
ansible_pass = WINDOWS_SERVER_PASS
server = WINDOWS_SERVER_IP

node {
   
    stage ('Checkout') {
    git branch: 'main',
       url: 'https://github.com/pravn-byte/kaseya-win-dev.git'
    }
    ansiblePlaybook( 
        playbook: 'ssh_win_access.yml',
        inventory: server + ',',
        extras: '-e ansible_user=' + ansible_user
		extras: '-e ansible_pass=' + ansible_pass
    )
    stage('clearout') {
        deleteDir()
    }
}
