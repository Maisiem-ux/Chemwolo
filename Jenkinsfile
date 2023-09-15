pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh'mvn clean package' 
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                sh'mvn test'
            }
        }
        stage('Code Analysis') {
            steps {
                //Use SonarQube to analyse code
            }
        }
        stage('Security Scan') {
            steps {
                //Perform a security scan using SonarQube with the OWASP Plugin
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Configure the staging environment to AWS EC2 instance
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                //run integration tests on the staging environment
            }
        }
        stage('Deploy to Production') {
            steps {
                //run integration tests on the staging environment
            }
        }
    }
    post {
        success {
            emailext(
                subject: "Pipeline Successful",
                body: "The Jenkins pipeline completed successfully.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
        failure {
            emailext(
                subject: "Pipeline Failed",
                body: "The Jenkins pipeline failed. Please check the logs for details.",
                to: 'maisiem716@gmail.com',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
    }
}pipeline {
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
        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production'
            }
        }
    }
    post {
        success {
            emailext(
                subject: "Pipeline Successful",
                body: "The Jenkins pipeline completed successfully.",
                to: 's222618352@deakin.edu.au',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
        failure {
            emailext(
                subject: "Pipeline Failed",
                body: "The Jenkins pipeline failed. Please check the logs for details.",
                to: 's222618352@deakin.edu.au',
                attachLog: true
                // attachmentsPattern: '**/console-log.txt'
            )
        }
    }
}
