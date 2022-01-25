pipeline{
    agent any
        stage('git checkout'){
                git branch: 'dev', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        stage('mkdir'){
                sh. 'mkdir project'
            }
        stage('cd'){
                sh. 'cd project'
            }
        stage('Cmake Build'){
                sh. 'cmake ..'
            }
        stage('Make'){
                sh. 'make'
          }
}
