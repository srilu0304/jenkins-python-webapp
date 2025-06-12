pipeline {
  agent any
  tools{
    'jenkins.plugins.shiningpanda.tools.PythonInstallation' 'Python3'
  }
  stages {
    stage('Install Requirements') {
      steps {
        bat 'pip install -r requirements'
      }
    }

    stage('run app') {
      steps {
        bat 'nohup python app.py &'
      }
    }

    stage('ping app') {
      steps {
        bat 'sleep 5 && curl http://localhost:5000'
      }
    }

  }
}
