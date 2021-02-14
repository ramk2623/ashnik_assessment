pipeline {
	agent node Ansible {
		stages {
			stage ('Deploy in Ansible'){
				steps {
					ansiblePlaybook colorized: true, credentialsId: '52.87.52.87', extras: '/home/ubuntu/ngnix_deploy.yml', installation: 'Ansible_Cloud', inventory: '/home/ubuntu/inventory_ashnik', playbook: '/home/ubuntu'
				}
			}
		}
	}
}