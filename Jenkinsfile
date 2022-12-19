pipeline{
    
    agent any 
    
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
