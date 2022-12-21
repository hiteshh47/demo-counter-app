pipeline{
    
    agent any 
    tools {
        maven 'h-maven'
        jdk 'h-jdk'
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
       stage('Integration Testing'){ 
            
         steps{
                
            script{
                    
                    sh 'mvn verify -DskipUnitTests'
                }
            }
        } 
       stage('Maven Build'){ 
            
         steps{
                
            script{
                    
                    sh 'mvn clean install'
                }
            }
        }   
     }
  }
