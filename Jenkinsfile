pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ShettyGagan/JenkinsDemo.git'
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
                bat 'venv\\Scripts\\activate && set PYTHONPATH=%CD% && pytest'

            }
        }
    }
}
