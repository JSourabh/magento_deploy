pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		echo 'create directory'
                sh 'mkdir /var/www/html/magent_pip'
		echo 'copy data'
		sh 'mv *.* /var/www/html/magent_pip'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
