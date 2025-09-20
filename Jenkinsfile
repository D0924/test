pipeline {
    agent any
    stages { //所有阶段
        stage('构建') { //stage定义一个阶段
            steps {
                sh 'mvn clean build'
            }
        }
    }
}