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
                sh 'make'
            }
        }
        stage('Unit_Test') {
            steps {
                sh 'cmake CMakeLists.txt'
                sh 'make'
                sh './executeTests'
            }
        }
       stage('CppCheck') {
            steps {
                sh 'cppcheck --enable=all --check-config *.cpp'
            }
        } 
    }
}
