pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/aishwaryakashyap13/second-project-on-node.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run App') {
            steps {
                sh '''
                pkill node || true
                nohup npm start &
                '''
            }
        }
    }
}