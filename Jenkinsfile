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
        stage('Run') {
            steps {
                sh 'C:\Program Files\Java\jdk-17 HelloWorld'
            }
        }
    }
}
