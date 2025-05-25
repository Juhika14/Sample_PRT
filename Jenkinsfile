pipeline {
    agent any

    stages {
        stage('Checkout Repository') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Juhika14/Sample_PRT.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i /home/ubuntu/jenkins/workspace/Sample_PRT/inventory play.yaml'
            }
        }
    }
}

