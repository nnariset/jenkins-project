pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'  // Install Maven tool in Jenkins
        jdk 'JDK 1.8'        // Install JDK in Jenkins
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-username/jenkins-sample-project.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'target/*.jar', fingerprint: true
            }
        }
    }
    post {
        always {
            junit 'target/surefire-reports/*.xml'
            cleanWs() // Clean workspace after build
        }
    }
}
