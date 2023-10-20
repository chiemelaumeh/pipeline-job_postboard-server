pipeline { 
    
    agent any
    
    stages {
        stage("Checkout"){
            steps { 
                checkout scm
            }
        }
        stage("Code coverage") { 
            steps {
                jacoco() 
                
            }
           }
          }
         }
