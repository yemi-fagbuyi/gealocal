pipeline {
    
    agent any
    triggers {
  pollSCM '* * * * *'
}
    stages {
        stage('code') {
            steps {
                echo 'Build Step'
                sleep 10
            }
        }
        stage('Test') {
            steps {
                echo 'Test step'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy Step'
                sleep 10
            }
        }
        stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
    }
}
