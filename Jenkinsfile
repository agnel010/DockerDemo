pipeline {
    agent {
        docker {
            image 'python:3.9'
        }
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/agnel010/DockerDemo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Flask App') {
            steps {
                sh 'nohup python app.py &'
            }
        }
    }
}
