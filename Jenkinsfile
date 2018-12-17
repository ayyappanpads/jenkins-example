pipeline {
 agent any
stages {
 stage('CodeCheckout') {
 steps {
 script {
    checkout scm
     /*def mvnHome = tool 'maven-3'
     def javaHome = tool 'JAVA_1.8'*/
     sh 'apt-get install -y default-jdk'
     sh 'sudo apt install -y maven'
   
     }
    }
   }
   
 stage('build customer app code') { 
 steps {
  script {
        /*def mvnHome = tool 'maven-3'
        def javaHome = tool 'JAVA_1.8'*/
        sh 'sudo apt install -y maven'
        sh 'mvn clean install'
    }
  }
 }
  stage('docker image code') { 
 steps {
  script {
        sh 'docker build -t ayyappanpads/jenkins17dec1 .'
        sh 'docker run -p 3002:8080 -d ayyappanpads/jenkins17dec1 -v /var/run/docker.sock:/var/run/docker.sock jenkins-docker'
    }
  }
 }
}
}
