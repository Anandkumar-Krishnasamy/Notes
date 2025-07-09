pipeline {
    agent any
    stages {
        stage('Clone'){
            steps{
                git branch: 'main', url: 'https://github.com/Anandkumar-Krishnasamy/my_http_request_sb.git'
            }
        }
        
        
        stage('Pack') {
            steps {
                    sh 'mvn clean install'
            }
        }
    }
}# Notes
