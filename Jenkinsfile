pipeline {
  agent any
  stages {
    stage('build') {
      agent {
        docker {
          image '8u151-jdk-slim'
        }
        
      }
      steps {
        sh './mvnw -Pprod clean package'
      }
    }
  }
}