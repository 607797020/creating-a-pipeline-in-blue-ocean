pipeline {
  agent any
  stages {
    stage('Code check out') {
      steps {
        sh 'svn co https://collaborate.bt.com/svn/dnp-project/trunk/src/GeneratePassword --username 607797020 --password SilentQQWW89 --non-interactive'
      }
    }
    stage('Build') {
      steps {
        sh '''mvn clean install
mvn site'''
      }
    }
  }
}