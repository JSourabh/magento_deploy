pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		echo 'create directory'
                sh 'mkdir /var/www/html/magent_pip'
		echo 'copy data'
		sh 'mv * /var/www/html/magent_pip'
		
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
		sh 'sudo chmod -R 755 /var/www/html/magent_pip'
		sh 'sudo chown -R sourabh:sourabh /var/www/html/magent_pip'
		sh 'cd /var/www/html/magent_pip'
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
