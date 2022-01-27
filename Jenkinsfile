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
                cmakeBuild buildDir: 'build', cleanBuild: true, installation: 'InSearchPath', sourceDir: '/var/lib/jenkins/workspace/pp2/'
            }
        }
        stage('Test') {
            steps {
                ctest 'var/lib/jenkins/workspace/pp2/'
            }
        }
        stage('Make'){
            steps{
                sh 'cd ./var/lib/jenkins/workspace/pp2/build/'
                sh 'pwd'
                sh 'make'
            }
        }
    }
}
