pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 1, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Init') {
            steps {
                sh """
                 ls -ltr
                """
            }
        }
        stage('Plan') {
            steps {
                sh "echo this is Test"
                sh 'sleep 10'
            }
        }
        stage('Deploy') {
            steps {
                sh "echo this is Deploy"
            }
        }