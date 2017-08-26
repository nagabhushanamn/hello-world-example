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
    			archive 'build/libs/**/*.jar'
    			junit 'target/**/*.xml'	
    		}
    
    }
}