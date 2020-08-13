pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat "mvn clean install"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat "mvn test"
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                 
            }
        }
        
    stage("Upload to AWS") {
      steps {
        withAWS(region:'us-east-1',credentials:'sk_devops_creds') {
          s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'SpringBootRestDemo-0.0.1-SNAPSHOT.jar', bucket:'sandeep-jenkins')
        }
      }
    }
}
