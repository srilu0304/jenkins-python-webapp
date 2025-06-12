pipeline {
  agent any
  stages {
    stage('Install Requirements') {
      steps {
        sh 'pip install -r requirements'
      }
    }

    stage('run app') {
      steps {
        sh 'nohup python app.py &'
      }
    }

    stage('ping app') {
      steps {
        sh 'sleep 5 && curl http://localhost:5000'
      }
    }

  }
}