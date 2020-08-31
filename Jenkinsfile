pipeline {
  agent { docker { image 'qnib/pytest' } }
  stages {
    stage('build') {
       steps {
          sh 'virtualenv venv && . venv/bin/activate && pip install -r requirements.txt && python tests.py'
     }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}
