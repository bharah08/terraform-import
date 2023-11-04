pipeline {
    agent any

    stages {
        stage('git-checkout') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/bharah08/terraform--pro-1.git']])
            }
        }
        stage('terraform-init') {
            steps {
                sh 'terraform init'
            }
        }
        stage('terraform-import') {
            steps {
                sh 'terraform import aws_instance.example i-0667cd385f9c5777c'
            }
        }
    }
}
