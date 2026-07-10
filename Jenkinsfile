pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Verify Ansible') {
            steps {
                sh 'ansible --version'
            }
        }

        stage('Run Playbook') {
            steps {
                sh 'ansible-playbook -i inventory repo.yml'
            }
        }
    }
}
