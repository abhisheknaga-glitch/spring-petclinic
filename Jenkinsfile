pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('static analysis') {
      steps {
        sh '''./mvnw clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://18.143.161.107:9000 \\
  -Dsonar.token=sqp_6f267de4e027279da4deef7b7708593ff7605b20'''
      }
    }

  }
}