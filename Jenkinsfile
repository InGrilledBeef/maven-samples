pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/InGrilledBeef/maven-samples', branch: 'master')
      }
    }

    stage('run') {
      steps {
        bat 'mvn clean test verify'
      }
    }

  }
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
}