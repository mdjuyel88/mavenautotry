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
        mail(subject: 'suceess', body: 'hi md juyel', to: 'mjuyelhaque@gmail.com')
      }
    }

  }
}