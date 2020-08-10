pipeline {
    agent any 
    stages {
        stage('Clone') { 
            steps {
                sh 'https://github.com/Sandeep-Shrestha7/SpringbootRestDemo.git'
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
