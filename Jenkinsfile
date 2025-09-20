pipeline {
    agent any
    stages { //所有阶段
        stage('构建') { //stage定义一个阶段
            steps {
                withDockerContainer('maven:3.9.11-amazoncorretto-24-debian') {
                                    // some block
                                    sh 'ls'
                                    sh 'pwd'
                                    sh 'mvn clean package'
                }
            }
        }
    }
}