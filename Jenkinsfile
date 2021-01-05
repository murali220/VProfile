pipeline {
  agent any
  parameters {
    choice(name: 'VERSION', choices: ['1.1.0' , '1.1.1' , '1.1.2'], description: '')
  }
  stages {
    stage("Build") {
      steps {
        echo 'Building application.....'
      }
    }
    stage("Test") {
      steps {
        echo 'Testing an application...'
      }
    }
  }
}
          
    
