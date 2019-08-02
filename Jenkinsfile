pipeline {
  agent {
    label 'MyNode'
  }
  publisher {
   mailer('2015pcecsmudit@poornima.org', true, true)
  }
  trigger {
    scm('* * * * *')
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
}
