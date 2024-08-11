pipeline {
    agent any

    stages {
        stage('Build & Test') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/final']], userRemoteConfigs: [[url: 'https://github.com/xanka/Udacity-eCommerce-Application.git']]])
                sh 'cd Application && mvn compile -DskipTests=true'
                
            }
        }
    }

    post {
        success {
            echo 'Process successfully!!'
        }

        failure {
            echo 'An error is occurred'
        }
    }
}
