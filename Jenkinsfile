pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/rohan-jagtap04/maven-samples-A6.git', branch: 'master')
      }
    }

    stage('test') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('verify') {
      steps {
        sh 'mvn verify'
      }
    }

    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('bisect') {
      steps {
        sh 'git bisect 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5 198644632661c67b6c32f59e9047c11a70685e15'
      }
    }

  }
  tools {
    maven 'DHT_MAVEN'
    jdk 'DHT_SENSE'
  }
}