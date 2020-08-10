node{
     
      stage('Checkout'){
         git 'https://github.com/Sandeep-Shrestha7/SpringbootRestDemo.git'
       
      }  
    
     stage('Compile Package'){
         def mvnHome = tool name: 'localMaven', type: 'maven'
          sh = "${mvnHome}/bin/mvn package"
        
    }
}


pipeline {
    agent any

    stages {
         
      stage('Checkout'){
         git 'https://github.com/Sandeep-Shrestha7/SpringbootRestDemo.git'
       
      }   
        stage ('Compile Stage') {

            steps {
                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn package"
            }
        }

        stage ('Testing Stage') {
                steps {
                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn test"
            }
           
        }


        stage ('Deployment Stage') {
           steps {
                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn deploy"
            }
        }
    }
}
