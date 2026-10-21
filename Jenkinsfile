pipeline {
    agent any

    tools {
        // Configure a Maven installation named "Maven3" in Jenkins,
        // or remove this tools block if Maven is already on PATH.
        maven 'Maven3'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Check Files') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                sh 'find . -name pom.xml'
            }
        }
        stage('Build and Test') {
            steps {
                sh 'mvn clean test'
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'Build and package completed successfully.'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
        always {
            echo 'Pipeline execution finished.'
        }
    }
}
