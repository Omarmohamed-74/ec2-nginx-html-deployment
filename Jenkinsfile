pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Omarmohamed-74/ec2-nginx-html-deployment.git'
            }
        }

        stage('Build') {
            steps {
                script {
                    try {
                        sh 'echo "building stage"'
                    } catch (Exception e) {
                        sh 'echo "exception found"'
                        throw e
                    }
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    if (env.BRANCH_NAME == "feat") {
                        sh 'echo "testing stage"'
                    } else {
                        sh 'echo "skipping testing stage"'
                    }
                }
            }
        }
    }
}
