pipeline {
  agent any
  stages {
    stage ('Compile') {
      steps {
        batchFile 'mvn clean compile'
      }
    }
  }
}
