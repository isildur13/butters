pipeline {
    agent any

    stages {
        stage('Build') {
            steps {

		go build butters-bottom.go 		
                
            }
        }
        stage('Test') {
            steps {

               ./butters-bottom

           }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
