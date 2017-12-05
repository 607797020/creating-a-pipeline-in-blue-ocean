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
        sh 'mvn -f ./GeneratePassword/pom.xml clean install site '
      }
    }
    stage('Codesonar') {
      steps {
        sh '''mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.3.0.603:sonar +
-f ./GeneratePassword/pom.xml +
Dsonar.projectKey=com.huettermann:all:master +
-Dsonar.login=admin +
-Dsonar.password=admin +
-Dsonar.language=java +
-Dsonar.sources=. +
-Dsonar.tests=. +
-Dsonar.test.inclusions=**/*Test*/** +
-Dsonar.exclusions=**/*Test*/**'''
      }
    }
  }
}