pipeline {
    agent dev-butters

    stages {
        stage('Build') {
            steps {

		sh '''
	             #!/bin/bash
		     go build butters-bottom.go 		
		     '''                
            }
        }
        stage('Test') {
            steps {
	        
            sh '''  ./butters-bottom '''

           }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
