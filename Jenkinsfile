pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                    def mvnHome = tool 'maven-3'
                    sh 'mvn clean compile'
                
            }
        }

        stage ('Testing Stage') {

            steps {
                    def mvnHome = tool 'maven-3'
                    sh 'mvn test'
                
            }
        }


        stage ('Deployment Stage') {
            steps {
                    def mvnHome = tool 'maven-3'
                    sh 'mvn deploy'
                
            }
        }
    }
}
