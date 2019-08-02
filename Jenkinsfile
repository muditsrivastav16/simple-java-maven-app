pipeline {
  agent any
  triggers {
    cron('* * * * *')
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
      mailer('2015pcecsmudit@poornima.org', true, true)
    }
  }
}
