pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/pgnaik/python_project.git']])
            }
        }
        stage('Build') {
            steps {
                git branch: 'main', url: 'https://github.com/pgnaik/python_project.git'
                bat 'python atm.py'
            }
        }
        stage('Test') {
            steps {
                echo "Python program is executing successfully...."
            }
        }
    }
}
