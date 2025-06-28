pipeline {
    agent none

    stages {
        stage('Clone Repository') {
            agent any
            steps {
                git branch: 'main',
                    url: 'https://github.com/Juhika14/Sample_PRT.git'
            }
        }

        stage('Run Ansible Playbook on Slave1') {
            agent { label 'Apache' }
            steps {
                script {
                    def playbookPath = "${env.WORKSPACE}/play.yaml"
                    def inventoryPath = "${env.WORKSPACE}/inventory.ini"
                    sh "ansible-playbook ${playbookPath} -i ${inventoryPath}"
                }
            }
        }

        stage('Run Ansible Playbook on Slave2') {
            agent { label 'Nginx' }
            steps {
                script {
                    def playbookPath = "${env.WORKSPACE}/play.yaml"
                    def inventoryPath = "${env.WORKSPACE}/inventory.ini"
                    sh "ansible-playbook ${playbookPath} -i ${inventoryPath}"
                }
            }
        }
    }
}
