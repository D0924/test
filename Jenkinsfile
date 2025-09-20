pipeline {
    agent any
    stages { //所有阶段
        stage('build') { //stage定义一个阶段
            steps {
            // 该步骤通常不应该在您的脚本中使用。请参考帮助查看详情。
            withDockerContainer(args: 'maven:4.0.0-rc-4-eclipse-temurin-17-noble', image: '') {
                sh 'ls'
                sh 'pwd'
                sh 'mvn clean build'
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