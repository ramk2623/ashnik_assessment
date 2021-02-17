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
	            git 'https://github.com/ramk2623/ashnik_assessment.git'   
	        }
	    }
		stage ('Deploy in Ansible'){
			steps {
				sh 'ansible-playbook -i /etc/ansible/hosts /home/ubuntu/Workspace/ashnik_playbook.yml'
		    }
	    }
    }
}
