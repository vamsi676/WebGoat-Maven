pipeline {
    agent {
        docker {
            image 'maven:latest' // Use the latest Maven image from Docker Hub
            args '-v /path/to/your/project:/workspace' // Mount the project directory as a volume
        }
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the GitHub repository
                git 'https://github.com/vamsi676/WebGoat-Maven.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build the project using Maven
                sh 'mvn clean install'
            }
        }
    }
}
