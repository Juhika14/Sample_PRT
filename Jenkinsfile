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
                ansiblePlaybook(
                    installation: 'ansible',
                    playbook: 'play.yaml',
                    syntaxCheck: true
                )
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                ansiblePlaybook(
                    installation: 'ansible',
                    playbook: 'play.yaml'
                )
            }
        }
    }
}
