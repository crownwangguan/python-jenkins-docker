pipeline {
  agent none
  stages {
    stage('Test') {
      agent {
        docker {
          image 'qnib/pytest'
        }

      }
      steps {
        sh 'py.test --verbose --junit-xml test-reports/results.xml sources/test_calc.py'
      }
    }
  }
}