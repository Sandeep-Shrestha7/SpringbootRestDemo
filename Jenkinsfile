pipeline {
    agent any

      stage('Checkout'){
         git 'https://github.com/Sandeep-Shrestha7/SpringbootRestDemo.git'
       
      }   
        stage ('Compile Stage') {

           
                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn package"
            
        }

        stage ('Testing Stage') {
              
                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn test"
           
           
        }


        stage ('Deployment Stage') {

                 def mvnHome = tool name: 'localMaven', type: 'maven'
                 sh = "${mvnHome}/bin/mvn deploy"
          
        }
    }
