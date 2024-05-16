pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'a1d9cc49-94ad-4a9a-b27a-970077cf856a', url: 'https://github.com/hkakjheeh/webapp.git']])
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
