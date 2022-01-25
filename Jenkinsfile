pipeline{
    agent any
    stages {
        stage('git checkout'){
            steps{
                git branch: 'dev', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('mkdir'){
            steps{
                sh. mkdir project
            }
        }
        stage('cd'){
            steps{
                sh. cd project
            }
        }
        stage('Cmake Build'){
            steps{
                sh. cmake ..
            }
        }
        stage('Make'){
            steps{
                sh. make
            }
        }
    }
}
