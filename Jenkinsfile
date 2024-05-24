pipeline {
    agent {
        docker {
            image 'maven:latest'
            args '-v /usr/lib/jvm/java-17-openjdk:/usr/lib/jvm/java-17-openjdk'
        }
    }
    
    environment {
        JAVA_HOME = '/usr/lib/jvm/java-17-openjdk'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from the GitHub repository
                git url: 'https://github.com/vamsi676/WebGoat-Maven', branch: 'main'
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
