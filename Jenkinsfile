pipeline {
  agent any
  environment {
	PATH = "/usr/bin/mvn:$PATH"
}
stages {
    stage("Checkout") {
      steps {
        git credentialsId: 'ec2-user', url: 'https://github.com/murali220/VProfile.git'
      }
    }
    stage("Test") {
      steps {
        echo 'Testing an application...'
      }
    }
   stage("Build") {
      steps {
        sh "mvn clean install"
        }
        }
  }
}
          
    
