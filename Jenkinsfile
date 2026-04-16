pipline{
     agent any
    
    
    tools{
        maven 'Maven'
        
       }
       
       
    stages {
         stage('Checkpoint') {
           
           steps {
           
             git branch: 'main' , url: "https://github.com/Reiyaan/MyMavenApp02.git"
           
           }
         }
         
         
         stage('Build') {
           
           steps {
           
             sh 'mvn clean package'
             
           }
         }
         
         
         stage('Test') {
           
           steps {
           
             sh 'mvn test'
             
           }
         }
         
         stage('Run Application') {
           
           steps {
           
             sh 'java -jar target/MyMavenApp02-1.0-SNAPSHOT.jar'
           }
         } 
    }      
           
post {
    success {
                  
           echo 'success'
           
    }        
           
    failure {
           echo 'fail'
           
    }              
    }       
}    
