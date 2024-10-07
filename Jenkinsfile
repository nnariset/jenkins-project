pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/nnariset/jenkins-project.git',
                    credentialsId: 'github-credentials', // Use the ID from Jenkins credentials
                    branch: 'main'
            }
        }
        // Other stages (e.g., Build, Test, etc.)
    }
}

*****************************************
