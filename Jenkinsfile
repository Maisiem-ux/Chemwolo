pipeline{
    agent any
    
    stages{
        stage('Build'){
            steps{
                //Build code using maven
                sh'mvn clean package'
                
            }
        }
        stage(' Unit and Integration Tests'){
            steps{
                // Run tests using JUnit
                sh'mvn test'
                
            }
             post{
                success{
                    emailext(
                    to:'s222618352@deakin.edu.au',
                    subject:'Unit and Integration Tests passed',
                    status:'The unit and integration Tests have passed.',
                    attachLog:true
                    )
                }
                failure{
                    emailext(
                    to:'s222618352@deakin.edu.au',
                    subject:'Unit and Integration Tests failed',
                    status:'The unit and integration Tests have failed.',
                    attachLog:true
                    )
                }
            }
        }    
        stage(' Code Analysis'){
            steps{
                //Use SonarQube to analyse code
                
            }
        }
        stage(' Security Scan'){
            steps{
                //Perform a security scan using SonarQube with the OWASP Plugin
                
            }
            post{
                success{
                    emailext(
                    to:'s222618352@deakin.edu.au',
                    subject:'Security Scan  passed',
                    body:'Security Scan have passed.'
                    attachLog:true //attachmentsPattern:'**'/console-log.txt'
                    )
                }
                failure{
                    emailext(
                    to:'s222618352@deakin.edu.au',
                    subject:'Security Scan  failed',
                    status:'Security Scan have failed.'
                    attachLog:true // attachmentsPattern:'**/console-log.txt'
                    )
                }
            }
        }
        stage(' Deploy to Staging'){
             environment{
                    // Configure the staging environment to AWS EC2 instance

                }
            steps{
                //Deploy the application to AWS EC2 instance
                
            }
        }
        stage('Integration Tests on Staging'){
            steps{
                //run integration tests on the staging environment
                
            }
        }
        stage(' Deploy to Production'){
            environment{
                //Configure the production environment to AWS EC2 environment
            }
            steps{
                //Deploy the application to AWS EC2 environment
                
            }
        }

    }
}
