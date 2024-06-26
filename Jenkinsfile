// Jenkins pipeline syntax
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Using a build automation tool like Maven for compiling and packaging your code
                echo 'Building code using Maven'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                // Using test automation tools like JUnit for unit tests and Selenium for integration tests
                echo 'Running unit tests and integration tests using JUnit and Selenium'
            }
            post {
                    success {
                    // Sending notification email with success status and logs attachment
                    echo 'Sending success notification email - Test'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Testing Successful",
                        body: "Tests using JUnit and Selenium is successful",
                        attachLog: true
                    )
                }
                failure {
                    // Sending notification email with failure status and logs attachment
                    echo 'Sending failure notification email - Test'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Testing failed",
                        body: "Tests using JUnit and Selenium failed",
                        attachLog: true
                    )
                    
                }
                
            }
        }
        stage('Code Analysis') {
            steps {
                // Integrating a code analysis tool like SonarQube to analyze code quality
                echo 'Running code analysis with SonarQube'
            }
        }
        stage('Security Scan') {
            steps {
                // Performing a security scan using a tool like OWASP ZAP
                echo 'Performing security scan with OWASP ZAP'
            }
            post {
                success {
                    // Sending notification email with success status and logs attachment
                    echo 'Sending success notification email - Security scan'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Security scan successful",
                        body: "Security scan with OWASP ZAP is sucessful",
                        attachLog: true
                    )
                    
                }
                failure {
                    // Sending notification email with failure status and logs attachment
                    echo 'Sending failure notification email - Security scan'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Security scan failed",
                        body: "Security scan with OWASP ZAP failed",
                        attachLog: true
                        )
                    
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                // Deploying the application to a staging server with AWS EC2
                echo 'Deploying to staging server with AWS EC2 instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                // Running integration tests on the staging environment with Selenium
                echo 'Running integration tests on staging environment using Selenium'
            }
            post {
                success {
                    // Sending notification email with success status and logs attachment
                    echo 'Sending success notification email - Integration test'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Integration test successful",
                        body: "Integration tests on staging environment using Selenium is sucessful",
                        attachLog: true
                    )
                    
                }
                failure {
                    // Sending notification email with failure status and logs attachment
                    echo 'Sending failure notification email - Integration test'
                    emailext (
                        to: "sathiyanarayanan.test@gmail.com",
                        subject: "Integration test failed",
                        body: "Integration tests on staging environment using Selenium failed",
                        attachLog: true
                        )
                    
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                // Deploying the application to a production server like AWS EC2
                echo 'Deploying to production server in AWS EC2 instance)'
            }
        }
    }
}
