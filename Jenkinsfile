pipeline {
  agent any
  triggers {
    cron('H * * * *')
  }
  stages {
    stage ('Compile') {
      steps {
        batchFile 'mvn clean compile'
      }
    }
    stage ('Test') {
      steps {
        batchFile 'mvn test'
      }
    }
  }
  post {
    always {
      echo 'post is executted'
    }
  }
}
