pipeline {

	agent {
			 any
			 custemWorkspace "/mnt/sagar"
			
	} 
	
	stages {
	
	stage('install-apache') {

	steps {

		sh "yum install httpd -y"

	}
	}
	
	stage('diploy-index') {

	steps {

		sh "cp -r dev.html /var/www/html"
		sh "chmod -R 777 /var/www/html"

	}
	}
	
	stage('restart-apache') {

	steps {

		sh "systemctl restart httpd"

	}
	}
}
}
