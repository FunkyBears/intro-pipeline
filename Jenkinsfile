pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('Prelim') {
      steps {
        echo 'Starting'
        sh 'echo true'
      }
    }
    stage('Ramping up') {
      steps {
        sleep 1
        input(message: 'Ready to go?', id: 'input', ok: 'Ready')
      }
    }
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}