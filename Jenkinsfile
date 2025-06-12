pipeline {
  agent any
  tools{
    'jenkins.plugins.shiningpanda.tools.PythonInstallation' 'Python3'
  }
  stages {
    stage('Install Requirements') {
      steps {
         bat 'python -m pip install -r requirements.txt'
      }
    }

    stage('run app') {
      steps {
        bat 'start /B python app.py'
      }
    }

    stage('ping app') {
      steps {
        bat 'curl http://localhost:5000'
      }
    }

  }
}
