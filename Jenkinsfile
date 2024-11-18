pipeline {
    agent any

    environment {
        ANSIBLE_PLAYBOOK = 'hello_world.yml'
		ANSIBLE_MY_TEXT = "${params.my_text}"
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/adrianang2024/mystudentpublicrepo.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    playbook: "${ANSIBLE_PLAYBOOK}"
                )
            }
        }
    }
}