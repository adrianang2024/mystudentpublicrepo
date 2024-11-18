pipeline {
    agent any

    environment {
        ANSIBLE_PLAYBOOK = '/tmp/hello_world.yml'
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