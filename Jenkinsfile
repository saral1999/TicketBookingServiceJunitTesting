pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                withMaven(maven : 'maven-plugin-3.16')
                sh 'mvn compile'
            }
        }
        stage('Test') { 
            steps {
                withMaven(maven : 'maven-plugin-3.16')
                sh 'mvn test' 
            }
        }
        stage('Deploy') { 
            steps {
               withMaven(maven : 'maven-plugin-3.16')
                sh 'mvn deploy'
            }
        }
    }
}
