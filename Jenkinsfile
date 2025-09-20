pipeline {
    agent any
    stages { //所有阶段
        stage('build') { //stage定义一个阶段
            steps {
                sh 'ls'
                sh 'pwd'
                sh 'mvn clean build'
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