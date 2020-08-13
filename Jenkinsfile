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
        withAWS(region:'us-east-1') {
            s3Upload(path:'C:/WINDOWS/system32/config/systemprofile/.m2/repository/org/test/SpringBootRestDemo/0.0.1-SNAPSHOT',file: 'SpringBootRestDemo-0.0.1-SNAPSHOT.jar', bucket:'sandeep-jenkins', path:'/path/to/targetFolder/')
         
        }
      }
    }
    }
}
