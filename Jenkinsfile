pipeline{
    agent{
        label 'WinSlave1'
    }
    stages {
        stage('git checkout'){
            steps{
                git branch: 'windows', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('Cmake Build'){
            steps{
                sh 'pwd'
                cmakeBuild buildDir: 'build', cleanBuild: true, installation: 'InSearchPath', sourceDir: 'C:/jenkins_slavenode/workspace/winpp/'
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
                sh 'cd C:/jenkins_slavenode/workspace/pp2/day01/src/'
                sh 'cppcheck --enable=all --check-config *.cpp'
            }
        } 
    }
}
