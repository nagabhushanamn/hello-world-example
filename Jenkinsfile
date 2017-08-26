pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                sh 'mvn package'
            }
        }
    }
    post{
    
    		always{
    			archive 'target/**/*.jar'
    			junit 'target/**/*.xml'	
    			mail to: 'nag@example.com',
	             subject: "Success Pipeline: ${currentBuild.fullDisplayName}",
	             body: "Something is wrong with ${env.BUILD_URL}"
	    		}
    		
    
    }
}