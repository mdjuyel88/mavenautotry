pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('clean') {
      steps {
        sh 'mvn clean'
      }
    }

    stage('compile') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('package') {
      steps {
        sh 'mvn package'
      }
    }

    stage('execute') {
      steps {
        sh '''chmod +x helloworld-4.0.jar
./helloworld-4.0.jar'''
      }
    }

  }
}