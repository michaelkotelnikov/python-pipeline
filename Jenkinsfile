pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
       steps {
          sh 'ls -l env && python3 -m pip install -r requirements.txt'
     }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}
