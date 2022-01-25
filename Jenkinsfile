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
                sh 'pwd'
                sh 'sudo apt install cmake'
                sh 'cd /var/lib/jenkins/workspace/pp2/'
                sh 'cmake ..'
            }
        }
        stage('Make'){
            steps{
                sh 'make'
            }
        }
    }
}
