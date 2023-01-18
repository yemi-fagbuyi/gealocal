pipeline {
    triggers {
        pollSCM('* * * * *')
    }
    agent any
    tools{
        maven 'M2_HOME'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn install'
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('create zipfile') {
            steps {
               sh'zip geaolocal${BUILD_NUMBER}.zip *  --exclude Jenkinsfile README.md'
                      
            }
        }
        stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
    }
}

