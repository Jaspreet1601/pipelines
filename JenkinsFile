pipeline {
    agent any
    tools {
        maven 'm1'
    }
    stages {
        stage("checkout") {
            steps {
                git branch: 'main', url: 'https://github.com/Jaspreet1601/pipelines.git'
            }
        }
        stage("clean") {
            steps {
                bat 'mvn clean'
            }
        }
        stage("validate") {
            steps {
                bat 'mvn validate'
            }
        }
        stage("compile") {
            steps {
                bat 'mvn compile'
            }
        }
        stage("test") {
            steps {
                bat 'mvn test'
            }
        }
        stage("package") {
            steps {
                bat 'mvn package'
            }
        }
        stage("integration-test") {
            steps {
                bat 'mvn integration-test'
            }
        }
        stage("verify") {
            steps {
                bat 'mvn verify'
            }
        }
        stage("install") {
            steps {
                bat 'mvn install'
            }
        }
        stage("deploy") {
            steps {
                bat 'mvn deploy:deploy-file' // Corrected the deploy command
            }
        }
    }
}
