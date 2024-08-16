pipeline {
    agent {
        label 'AGENT-1'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Init') {
            steps {
               sh """
                cd 01-vpc
                terraform init -reconfigure
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
    }
}