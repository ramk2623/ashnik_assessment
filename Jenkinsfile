pipeline {
    agent {
        node {
            label "ansible" 
            customWorkspace '/home/ubuntu/Workspace'    
        }
    }
    
    stages {
	    stage ('Clone from GitHUB'){
	        steps {
	            cleanWs()
	            git 'https://github.com/ramk2623/ashnik_assessment.git'   
	        }
	    }
		stage ('Deploy in Ansible'){
			steps {
				ansiblePlaybook colorized: true, credentialsId: '54.88.81.12', extras: '-vvvv', installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: 'ashnik_playbook.yml'
		    }
	    }
    }
}
