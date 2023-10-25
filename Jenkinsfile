pipeline {
    agent any
    
    tools {
        // Specify the name of the Git tool configured in Jenkins.
        git 'Git'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }
        stage('Test') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }
}
