pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    userRemoteConfigs: [[url: 'https://github.com/manthanindane/AssignmentNo8.git']],
                    extensions: [[$class: 'WipeWorkspace'], [$class: 'CleanCheckout']]
                ])
            }
        }
        stage('Build') {
            steps {
                script {
                    def gitExe = tool name: 'Git', type: 'Tool'
                    sh script: "${gitExe}/bin/git pull", returnStatus: true
                }
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
