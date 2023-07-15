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
        sh '''./mvn sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://172.31.7.83:9000 \\
  -Dsonar.token=sqp_c7cf25260bd566cd4967ca32d2df69a6f1480494'''
      }
    }

  }
}