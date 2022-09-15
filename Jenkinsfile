pipeline {
     agent any
     tools {
        gradle "gradle"
        jdk "java11"
    }
     stages {
         stage('Clean Workspace') {
             steps {
                  deleteDir()                  
             }
         }
         stage('Clone Project') {
             steps {                  
                  checkout scm                  
             }
         }
         stage('Build') {
             steps {    
                  sh 'java -version'
                  sh 'chmod +x gradlew'
                  sh './gradlew clean build --debug --stacktrace'
             }              
         }
     }
 }
