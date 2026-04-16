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
           
             sh 'mvn exec:java -Dexec.mainClass="com.example.App"
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
