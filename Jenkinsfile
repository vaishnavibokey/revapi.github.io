pipeline {
    agent any

    stages {
        stage('download_install_apache') {
            steps {
                sh "sudo yum install httpd -y"
                sh "java -version"

            }
        }
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
                sh "echo 'This is my apache server' >> index.html"
				sh "sudo cp -r index.html /var/www/html"
            }
        }
    }
}
