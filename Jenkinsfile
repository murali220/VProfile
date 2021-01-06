pipeline {
  agent any
  stages {
    stage("Checkout") {
      steps {
        git credentialsid: 'git', url: 'https://github.com/murali220/VProfile.git'
      }
    }
    stage("Test") {
      steps {
        echo 'Testing an application...'
      }
    }
  }
}
          
    
