pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Clone') {
            steps {
               script {
                   git "https://github.com/Tejaswee12/homepage-app-springboot-jar.git"
                   
               }
            }
        }
       
        stage('Maven') {
            steps {
               sh '''mvn package'''
            }
        }
         stage('View Files') {
            steps {
               script {
                  sh '''ls target'''
                } 
            }
        }
    }
}
