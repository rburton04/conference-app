pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'test jenkins file'
      }
    }
    stage('Integration') {
      steps {
        parallel(
          "Integration": {
            echo 'build docker'
            
          },
          "Branch1 Spec1": {
            echo 'API 1'
            
          },
          "Branch2 Spec2": {
            echo 'API 2'
            
          },
          "Integration before QA": {
            echo 'Integration'
            
          }
        )
      }
    }
    stage('QA') {
      steps {
        echo 'QA'
      }
    }
    stage('PreProd') {
      steps {
        echo 'PreProd'
      }
    }
    stage('Reports') {
      steps {
        echo 'Reports'
      }
    }
  }
}