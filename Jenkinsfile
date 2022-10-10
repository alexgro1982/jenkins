pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/alexgro1982/example-playbook.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook inventory: 'inventory/prod.yml', playbook: 'site.yml'
            }
        }
    }
}
