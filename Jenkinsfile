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
		stage("Deploy") {
      steps {
	  sshagent(['tomcat_deploy']) {
    sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Nuxus_Pipeline/target/vprofile-v1.war ec2-user@65.0.170.15:/opt/apache-tomcat-8.5.61/webapps"
} 
        }
        }
  }
}
