pipeline {
	agent node ansible {
	ws('/home/ubuntu/workspace') {
}
		stages {
			stage ('Clone from GitHub') {
				steps {
					git 'https://github.com/ramk2623/ashnik_assessment.git'
				}
			}
			stage ('Deploy in Ansible'){
				steps {
					ansiblePlaybook colorized: true, credentialsId: '52.87.52.87', extras: '/home/ubuntu/ngnix_deploy.yml', installation: 'Ansible_Cloud', inventory: '/home/ubuntu/inventory_ashnik', playbook: '/home/ubuntu'
				}
			}
		}
	}
}