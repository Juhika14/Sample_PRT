pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/Juhika14/Sample_PRT.git'
            }
        }

        stage('Syntax Check') {
            steps {
                sh 'ansible-playbook play.yaml --syntax-check'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook play.yaml'
            }
        }
    }
}
