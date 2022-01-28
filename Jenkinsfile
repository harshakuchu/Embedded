pipeline{
    agent{
        label 'LinSlave'
    }
    stages {
        stage('git checkout'){
            steps{
                git branch: 'dev', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('Cmake Build'){
            steps{
                cmakeBuild buildDir: 'build', cleanBuild: true, installation: 'InSearchPath', sourceDir: '/var/lib/jenkins/workspace/pp2/'
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
                sh 'cd var/lib/jenkins/workspace/pp2/day01/src/'
                sh 'cppcheck --enable=all --check-config *.cpp'
            }
        } 
    }
}
