pipeline {
    agent any

    stages {
            stage ('pre') {

                steps {
                sh 'sudo rm -rf /var/www/html/*'
                sh 'sudo rm -rf /var/www/html/.git'
	             }
		 }
                 
        

		stage ('install') {
		 steps {
                      sh 'sudo yum install httpd  -y'
                    }
                  }


		stage('start service') {
		  steps {
                       sh 'sudo systemctl start httpd'
                      }
		}

		stage('git clone') {
		steps {
                	sh 'sudo git clone https://github.com/ashwin1-dev/web-27.git  /var/www/html '
                      }
                  }
          }
    
}

