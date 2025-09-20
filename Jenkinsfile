pipeline {
    agent any
    stages { //所有阶段
        stage('build') { //stage定义一个阶段
            steps {
            withDockerContainer(
            args: '-v /usr/local/Cellar/maven/3.9.11/libexec/conf:/usr/share/maven/conf -v /usr/local/Cellar/maven/3.9.11/libexec/conf:/root/.m2',
            image:'maven:3.9.11-amazoncorretto-8') {
             sh 'ls'
             sh 'pwd'
             sh 'mvn clean'
            }
              }
                }
        stage('package') {
            steps {
                echo '打包  ok...'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy ok...'
            }
        }
    }
}