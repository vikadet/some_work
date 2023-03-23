pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "This is a test" + $name > newfile.txt'
      }
    }

    stage('Post') {
      steps {
        archiveArtifacts(artifacts: 'newfile.txt', fingerprint: true, onlyIfSuccessful: true)
      }
    }

  }
  environment {
    name = ''
  }
}