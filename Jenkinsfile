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
            s3Upload(file:'C:\WINDOWS\system32\config\systemprofile\.m2\repository\org\test\SpringBootRestDemo\0.0.1-SNAPSHOT\SpringBootRestDemo-0.0.1-SNAPSHOT.jar', bucket:'sandeep-jenkins', path:'/path/to/targetFolder/')
         
        }
      }
    }
    }
}
