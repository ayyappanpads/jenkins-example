pipeline {
    agent any
  
    stages {
         stage('build customer app code') { 
 steps {
  script {
        def mvnHome = tool 'maven-3'
        sh 'mvn clean install'
    }
  }
 }
    
        
        stage ('Compile Stage') {

            steps {
                    sh 'mvn clean compile'
                
            }
        }

        stage ('Testing Stage') {

            steps {

                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
                    sh 'mvn deploy'
                
            }
        }
    }
}
