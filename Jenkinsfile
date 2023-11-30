pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                script {
                    // Cloning repository
                   git 'https://github.com/pswathi2203/docjen.git'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    sh 'docker build -t jenkinsimg .'
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    // Run tests if needed
                    sh 'docker run -it jenkinsimg'
                }
            }
        }
    }
}
