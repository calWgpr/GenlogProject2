pipeline {
    agent any

    tools {
        maven "M3"   // uses the Maven installation configured in Jenkins
    }

    stages {
        stage('Checkout') {
           steps {
            git branch: 'main', url: 'https://github.com/your-user/your-repo.git'
           }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage (customize as needed)'
            }
        }
    }
}
