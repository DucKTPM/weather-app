pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                // Clone mã nguồn từ GitHub
                git 'https://github.com/hoata671/weather-app.git' // Thay đổi link này thành URL của repository của bạn
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Lệnh để triển khai lên AwardSpace
                    def command = 'put -r * /home/www//myweatherhi.atwebpages.com/' // Thay đổi đường dẫn này
                    bat "winscp.com /command \"open 4519755:Maihoa@813@myweatherhi.atwebpages.com\" \"$command\" \"exit\""
                }
            }
        }
    }

    post {
        success {
            echo 'Deploy thành công!'
        }
        failure {
            echo 'Deploy thất bại!'
        }
    }
}
