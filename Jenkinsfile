pipeline {
    agent any

    stages {     
           stage('start_httpd') {
            steps {
                sh "sudo service httpd start"
            }
        }
		stage('status_check') {
            steps {
                sh "sudo service httpd status"
            }
        }
		stage('deploy_httpd') {
            steps {
                sh "echo 'new datar' >> index.html"
				sh "sudo cp -r index.html /var/www/html"
            }
        }
    }
}
