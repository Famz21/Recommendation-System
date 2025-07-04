pipeline {
    agent any

    stages{
        stage("Cloning from github repository"){
            steps{
                script{
                    echo 'cloning from github repository'
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-token', url: 'https://github.com/Famz21/Recommendation-System.git']])
                }
                
            }
        }
    }
}