pipeline {
  agent none
  stages {
    stage('Check-out code') {
      steps {
        svn(changelog: true, poll: true, url: 'https://collaborate.bt.com/svn/dnp-project/trunk/src/GeneratePassword')
      }
    }
  }
}