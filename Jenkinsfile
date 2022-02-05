pipeline {
    agent any

    stages {
        stage('构建') {
            steps {
                script {
                    echo '构建中...'
                    sleep(1)
                }
            }
        }

        stage('测试') {
            steps {
                script {
                    echo '测试中...'
                    sleep(1)
                }
            }
        }
        
        stage('部署') {
            steps {
                script {
                    echo '部署中...'
                    sleep(1)
                }
            } 
        }

    }
    post {
            always {
                echo 'pipeline have finished'
                //lgSendBuildInfo() 也可以不传options
                lgSendBuildInfo(options: ['env':'生产环境', '版本':'1.0.0'])
            }
    }
}