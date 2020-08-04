pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		echo 'create directory on jenkins'
                sh 'mkdir /var/www/html/magento_2'
		echo 'copy data one path to another'
		sh 'mv * /var/www/html/magento_2'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh 'sudo cd /home/sourabh'
		sh 'sudo chmod -R 755 /var/www/html/magento_2'
		sh 'sudo chown -R sourabh:sourabh /var/www/html/magento_2'
		sh 'cd /var/www/html/magento_2'
		sh 'sudo chmod -R 777 pub var app generated'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
