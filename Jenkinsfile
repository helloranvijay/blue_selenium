pipeline {
  agent any
  stages {
    stage('Initialize') {
      agent any
      steps {
        bat 'echo "hello"'
        bat 'cd C:\\Users\\RANVZ\\eclipse-workspace\\Saatvik_I'
        bat 'java -version'
      }
    }
    stage('Execute') {
      steps {
        bat 'C:\\Users\\RANVZ\\eclipse-workspace\\Saatvik_I\\start.bat'
      }
    }
    stage('send email') {
      steps {
        emailext(subject: 'Test Success', body: 'Selenium Script Execution was a success', attachLog: true, from: 'no-reply@ranvijay.in', replyTo: 'no-reply@ranvijay.in', to: 'hello@ranvijay.in')
      }
    }
  }
}