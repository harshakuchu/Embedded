pipeline{
    agent any
    stages {
        stage('git checkout'){
            steps{
                git branch: 'feature', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('Cmake Build'){
            steps{
                cmake arguments: 'cmake ..', installation: 'InSearchPath', workingDir: '/var/lib/jenkins/workspace/pp2/'
            }
        }
        stage('Make'){
            steps{
                sh 'make'
            }
        }
    }
}
