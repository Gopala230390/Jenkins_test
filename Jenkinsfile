pipeline {
    agent any
    
    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('Checkout') {
            steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/devopscbabu/DevOpsAddressBook.git']]])
            }
        }
        stage('Compile') {
            steps {
            sh 'mvn compile'
            }
        }  
        stage('Test') {
            steps {
            sh 'mvn test'
            }
        }
     
           
    }
}
