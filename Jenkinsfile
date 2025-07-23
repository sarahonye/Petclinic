pipeline {
    agent any
    tools {
        jdk 'jdk11'
        maven 'maven'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature-1', url: 'https://github.com/sarahonye/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
         stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
          
    }
}
