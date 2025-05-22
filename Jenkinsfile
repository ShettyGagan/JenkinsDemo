pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ShettyGagan/JenkinsDemo.git'
            }
        }

        stage('Install Dependencis') {
            steps {
                bat 'python -m venv venv'
                bat 'venv\\Scripts\\activate && pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'venv\\Scripts\\activate && pytest'
            }
        }
    }
}
