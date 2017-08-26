pipeline {
    agent {
        docker { image 'maven' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
    post{
    
    		always{
    			junit 'target/**/*.xml'	
    		}
    
    }
}