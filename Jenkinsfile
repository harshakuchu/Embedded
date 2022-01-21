pipeline{
    agent any
    stages {
        stage('git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('Cmake Build'){
            steps{
                cmakeBuild buildDir: 'build', cleanBuild: true, installation: 'InSearchPath', sourceDir: '/home/ubuntu/Embedded/'
            }
        }
    }
}
