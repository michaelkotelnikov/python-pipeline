pipeline {
  agent { docker { image 'python:3.7.2' } }
  stages {
    stage('build') {
       steps {
          sh 'python3 -m venv env && . ./env/bin/activate && python3 -m pip install -r requirements.txt'
     }
    }
    stage('test') {
      steps {
        sh '. ./env/bin/activate && python3 tests.py'
      }   
    }
  }
}
