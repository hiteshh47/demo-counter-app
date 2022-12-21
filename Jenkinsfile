pipeline{
    
    agent any 
    tools {
        maven 'maven'
        jdk 'java11'
    }
    stages {
        
        stage('Git Checkout'){
            
            steps{
                
                script{
                    
                    git branch: 'main', url: 'https://github.com/hiteshh47/demo-counter-app.git'
                }
            }
        }
      stage('Unit Testing'){ 
            
         steps{
                
            script{
                    
                    sh 'mvn test'
                }
            }
        }    
     }
  }
