pipeline{
    agent{
        label 'LinSlave1'
    }
    stages {
        stage('git checkout'){
            steps{
                git branch: 'raja', url: 'https://github.com/harshakuchu/Embedded.git'
            }
        }
        stage('Cmake Build'){
            steps{
                sh 'pwd'
                cmakeBuild buildDir: 'build', cleanBuild: true, installation: 'InSearchPath', sourceDir: '/home/raja/workspace/pp1/'
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
                sh 'cd /home/raja/workspace/pp2/day01/src/'
                sh 'cppcheck --enable=all --check-config *.cpp'
            }
        } 
    }
}
