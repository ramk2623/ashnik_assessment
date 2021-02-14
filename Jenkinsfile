pipeline {
    agent {
        node {
            label "Ansible" 
            customWorkspace '/home/ubuntu/workspace'    
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
				ansiblePlaybook colorized: true, credentialsId: '52.87.52.87', installation: 'Ansible_Cloud', inventory: '/home/ubuntu/inventory_nginx', playbook: '/home/ubuntu/ngnix_deploy.yml'
		    }
	    }
    }
}