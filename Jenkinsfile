pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Using a build automation tool like Maven to compile and package your code
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
                    emailext(to: "sathiyanarayanan.test@gmail.com",
                        subject: "Testing Successful",
                        body: "Tests using JUnit and Selenium were successful")
                }
                failure {
                    // Sending notification email with failure status and logs attachment
                    echo 'Sending failure notification email - Test'
                    emailext(to: "sathiyanarayanan.test@gmail.com",
                        subject: "Testing Failed",
                        body: "Tests using JUnit and Selenium failed")
                }
            }
        }
    }
}
