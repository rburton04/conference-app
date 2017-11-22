pipeline {
  agent none
  stages {
    stage('Dev') {
      steps {
        echo 'test jenkins file'
      }
    }
    stage('error') {
      steps {
        parallel(
          "Branch 1": {
            echo 'build docker'
            
          },
          "Branch 2": {
            echo 'branch 2'
            
          },
          "Integration before QA": {
            echo 'integration'
            
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