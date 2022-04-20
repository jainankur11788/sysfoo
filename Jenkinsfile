pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'compiling sysfoo app'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'Running tests'
        sh 'mvn compile test'
      }
    }

    stage('package') {
      steps {
        echo 'packaging sysfoo app'
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/*.war'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
  post {
    always {
      echo 'This pipeline is completed..'
    }

  }
}