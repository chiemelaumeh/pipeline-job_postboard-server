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

        stage("Build") {
            steps {   
            sh "npm install"  
            // sh "nodemon server.js"
        
            }
        }
        stage("Publish Artifacts") {
            steps {   
            sh "set +x && echo \"//ec2-52-15-146-91.us-east-2.compute.amazonaws.com:8081/repository/postboard-server_hosted/:_authToken=NpmToken.2843eecf-c55f-3155-9788-2091229be97a\" >> .npmrc"
            sh "npm publish"
            }
        }
          }
         }
