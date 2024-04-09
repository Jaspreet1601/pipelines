pipeline{
    agent any
    tools {maven 'm1'}
    stages {
        stage('Checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/Jaspreet1601/JenkinsPipeline.git'
            }
        }
        stage('Build'){
            steps {
                bat 'mvn clean install'
            }
        }
        stage('test'){
            steps {
                bat 'mvn test'
            }
        }
        stage('Package'){
            steps{
                bat 'mvn package'
            }
        }
        stage('Result'){
            steps{
                bat 'java -cp target/mavenproject-1.0-SNAPSHOT.jar com.example.App'
            }
        }
    }
}
