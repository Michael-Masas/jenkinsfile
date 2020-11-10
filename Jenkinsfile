pipeline { 
    agent any
    stages {
        stage('Build') { 
            steps {
	      script {
	       docker.build("microblog-image")
	       docker run --name microblog-con -d -p 8000:5000 microblog-image:latest
                  }
            }
	}
                        }
        post {
            success {
                echo "Pipeline successful"
        }
	    failure {
		 echo "The Pipeline failed :("
		    }
	}
	 }
