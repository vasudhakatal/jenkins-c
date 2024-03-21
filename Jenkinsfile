pipeline {
    agent any
    stages {
        // make build
        stage('Build') {
            steps {
                echo "Fetching the source code from GitHub"
                echo "Compiling the code and generating artifacts."
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit tests: started"
                echo "Running integration tests: started"
            }
            post {
                success {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Unit and Integration Tests Success',
                        body: 'The unit and integration tests have succeeded. Find attached logs for more information.'
                }
                failure {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Unit and Integration Tests Failed',
                        body: 'The unit and integration tests have failed. Find attached logs for more information.'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Running code analysis: started"
            }
        }
        stage('Security Scan') {
            steps {
                echo "Running security scan: started"
            }
            post {
                success {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Security Scan Success',
                        body: 'The Security Scan has succeeded. Find attached logs for more information.'
                }
                failure {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Security Scan Failed',
                        body: 'The Security Scan has failed. Find attached logs for more information.'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploying to Staging: started"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on Staging: started"
            }
            post {
                success {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Integration Tests on Staging Success',
                        body: 'The Integration Tests on Staging have succeeded. Find attached logs for more information.'
                }
                failure {
                    mail to: 'vasudha4859.be22@chitkara.edu.in',
                        subject: 'Integration Tests on Staging Failed',
                        body: 'The Integration Tests on Staging have failed. Find attached logs for more information.'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying to Production: started"
            }
        }
    }
}
