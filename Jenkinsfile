pipeline {

    agent any

    stages {

        stage('Build') {

            steps {

                echo 'Build using Maven' 

            }

        }

        stage('Unit and Integration Tests') {

            steps {

                echo 'Run Unit and Integration Tests using Selenium'

            }

        }

        stage('Code Analysis') {

            steps {

                echo 'Integrate code analysis using SonarQube'

            }

        }

        stage('Security Scan') {

            steps {

                echo 'Use Owasp Zap to identify any vulnerabilities'

            }
            post {

        success {

            emailext(

                subject: "Security Scan Successful",

                body: "Security Scan completed successfully.",

                to: 'maisiem716@gmail.com',

                attachLog: true

                // attachmentsPattern: '**/console-log.txt'

            )

        }

        failure {

            emailext(

                subject: "Security Scan Failed",

                body: "Security Scan has failed. Please check the logs for details.",

                to: 'maisiem716@gmail.com',

                attachLog: true

                // attachmentsPattern: '**/console-log.txt'

            )

        }

    }

        }

        stage('Deploy to Staging') {

            steps {

                echo 'Deploy to Staging using AWS CLI'

            }

        }

        stage('Integration Tests on Staging') {

            steps {

                echo 'Run integration tests on staging using JUnit'

            }
            post {

        success {

            emailext(

                subject: "Test was Successful",

                body: "Test completed successfully.",

                to: 'maisiem716@gmail.com',

                attachLog: true

                // attachmentsPattern: '**/console-log.txt'

            )

        }

        failure {

            emailext(

                subject: "Test Failed",

                body: "Test failed. Please check the logs for details.",

                to: 'maisiem716@gmail.com',

                attachLog: true

                // attachmentsPattern: '**/console-log.txt'

            )

        }

    }

        }

        stage('Deploy to Production') {

            steps {

                echo 'Deploy to Production'

            }

        }

    }

    

}
