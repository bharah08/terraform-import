pipeline {
    agent any

    stages {
        stage('git-checkout') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/bharah08/terraform--pro-1.git']])
            }
        }
        stage('Hello') {
            steps {
                sh 'terraform init'
            }
        }
        stage('Hello') {
            steps {
                sh 'terraform import aws_instance.example i-0667cd385f9c5777c'
            }
        }
    }
}
