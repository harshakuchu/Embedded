pipeline{
    agent any
    stages {
        stage('git checkout'){
            steps{
                git branch: 'feature', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('changing directory'){
            steps{
                sh 'cd build'
            }
        }
        stage('Cmake Build'){
            steps{
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
