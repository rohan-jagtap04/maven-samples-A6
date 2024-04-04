pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/rohan-jagtap04/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean && mvn verify && mvn test'
      }
    }

  }
  tools {
    maven 'DHT_MAVEN'
    jdk 'DHT_SENSE'
  }
}