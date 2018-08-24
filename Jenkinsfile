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
    stage('Checkpoint') {
      steps {
        checkpoint 'Checkpoint'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
    stage('Ramping up') {
      input {
        message 'Ready to go?'
        id 'Ready'
        parameters {
          choice(name: 'APP_VERSION', choices: '''v1.1
v1.2
v1.3''', description: 'What to deploy?')
        }
      }
      steps {
        sleep 1
      }
    }
  }
}