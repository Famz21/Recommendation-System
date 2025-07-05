pipeline {
    agent any

    environment{
        VENV_DIR = 'venv'
    }

    stages{
        stage("Cloning from github repository"){
            steps{
                script{
                    echo 'cloning from github repository'
                    checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'github-token', url: 'https://github.com/Famz21/Recommendation-System.git']])
                }
                
            }
        }
        stage("Making virtual environment"){
            steps{
                script{
                    echo 'Making virtual environment'
                    sh '''
                    python -m venv ${VENV_DIR}
                    . ${VENV_DIR}/bin/activate
                    pip install --upgrade pip
                    pip install -e .
                    pip install dvc
                    '''
                }
                
            }
        }
    }
}