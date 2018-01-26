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
        echo 'Starting the build!'
        sh '''echo "current path:" `pwd`
echo "list contents of current path:"
ls -l'''
        echo 'let\'s try maven! :-)'
        sh './mvnw -Pprod clean package'
      }
    }
  }
}