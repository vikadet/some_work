pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'chmod +x ./testscript.sh'
        sh './testscript.sh > newfile.txt'
        sh 'echo "Ran the shell script" '
      }
    }

    stage('Post') {
      steps {
        archiveArtifacts(artifacts: 'newfile.txt', fingerprint: true, onlyIfSuccessful: true)
      }
    }

  }
}