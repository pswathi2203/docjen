pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                script {
                    // Cloning repository
                   git clone https://github.com/pswathi2203/docjen.git
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build Docker image
                    docker build -t jenkinsimg .
                }
            }
        }

        stage('Run') {
            steps {
                script {
                    // Run tests if needed
                    docker run -it jenkinsimg
                }
            }
        }
 }
