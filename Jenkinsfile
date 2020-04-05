pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

		bash '''
	             #!/bin/bash
		     go build butters-bottom.go 		
		     '''                
            }
        }
        stage('Test') {
            steps {
	        
            bash '''  ./butters-bottom '''

           }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
