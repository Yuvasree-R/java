pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Yuvasree-R/java.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deploy stage'
            }
        }

    }

    post {
        success {
            bat 'echo Build Successful'
        }

        failure {
            bat 'echo Build Failed'
        }
    }
}
