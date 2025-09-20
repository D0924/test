pipeline {
    agent any
    stages { //所有阶段
     stage('检查 docker') {
                steps {
                    // 验证 Docker 命令是否存在
                    sh 'docker --version'

                    // 验证 Docker 服务是否可访问（运行测试容器）
                    sh 'docker run --rm hello-world'
                }
            }
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