pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat "mvn clean install"
            }
        }
        
    stage("Upload to AWS") {
      steps {
         
        withAWS(region:'us-east-1', credentials: '1234567') {
            s3Upload(file:'target/SpringBootRestDemo-0.0.1-SNAPSHOT.jar', bucket:'sandeep-jenkins', path:'path/to/target/SpringBootRestDemo-0.0.1-SNAPSHOT.jar')
           
         
        }
      }
    }
    }
}
