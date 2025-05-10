pipeline {
    agent any
    
    tools {
        maven 'maven3.9'
        jdk 'jdk11'
    }
    
    stages {
        stage('Git Repo Checkout') {
            steps {
               git branch: 'dev', url: 'https://github.com/techpentest/Boardgame.git'
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
        
         stage('Validation') {
            steps {
                sh 'mvn validate'
            }
        }
        
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
