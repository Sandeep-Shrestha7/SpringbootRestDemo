pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat "mvn clean"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                bat "mvn test"
            }
        }
        
        stage('artifact') {
         archive 'target/*.jar'   
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                 
            }
        }
    }
}
