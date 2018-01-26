pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        node {
          label 'ACI-container'
        }
        
      }
      steps {
        sh './mvnw -Pprod clean package'
      }
    }
  }
}