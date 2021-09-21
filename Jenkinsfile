pipeline {
    agent any

    stages {
        stage('Start') {
            steps {
                echo 'Building..'
            }
        }
        
        stage('Deploy') {
            steps {
                ssh jenkins@172.31.95.45 rm -rf MyFirstRepo
                ssh jenkins@172.31.95.45 git clone https://github.com/jyothireddy425/MyFirstRepo.git
                ssh jenkins@172.31.95.45 cd MyFirstRepo
                ssh jenkins@172.31.95.45 cp -r mysite/* /var/www/html/
                ssh jenkins@172.31.95.45 cd -
            }
        }
    }
}
