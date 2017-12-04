pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Check-out code') {
      steps {
        svn(changelog: true, poll: true, url: 'https://collaborate.bt.com/svn/dnp-project/trunk/src/GeneratePassword')
      }
    }
  }
}