pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('clean') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('compile') {
      steps {
        sh 'mvn package'
      }
    }

    stage('package') {
      steps {
        sh 'mvn install'
      }
    }

    stage('execute') {
      steps {
        sh 'mvn exec:java'
      }
    }

  }
}