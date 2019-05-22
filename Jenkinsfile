pipeline {
  agent {
    label "jenkins-go"
  }
  environment {
    ORG = 'upendrasahu'
    APP_NAME = 'pipeline1'
    CHARTMUSEUM_CREDS = credentials('jenkins-x-chartmuseum')
  }
  stages {
    stage('Stage 1') {
      when {
        branch 'master'
      }
      steps {
        container('go') {
          sh "echo testpipeline"
        }
      }
    }
    stage('Stage 2') {
      when {
        branch 'master'
      }
      steps {
        container('go') {
          sh 'echo testpipeline'
        }
      }
    }
  }
}