pipeline 
{
    agent { label 'dev-butters' } 
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

	    sh '''cp -a butters-bottom /bin/ '''

	    archiveArtifacts 'butters-bottom'

            }
	}

	stage('Removing the Workspace..')
	{
	   steps {

		step([$class: 'WsCleanup'])
	    }
	}
	stage('Testing..')
	{
	    steps {
		
	    sh ''' butters-bottom '''

	    }	
	}
        
    
     }   
}    
