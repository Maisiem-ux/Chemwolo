pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building' 
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and Integration Tests'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Code Analysis'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Security Scan'
            }
        }
        post {
        success {
            emailext(
                subject: "Pipeline Successful",
                body: "Security Scan  passed.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
        failure {
            emailext(
                subject: "Pipeline Failed",
                body: "Security Scan  failed.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
    }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging'
            }
        }
        post {
        success {
            emailext(
                subject: "Pipeline Successful",
                body: "Unit and Integration Tests passed.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
        failure {
            emailext(
                subject: "Pipeline Failed",
                body: "Unit and Integration Tests failed.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
    }
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production'
            }
        }
    }
    
}
