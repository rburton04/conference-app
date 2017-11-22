pipeline {
  agent {
    dockerfile {
      filename 'dockerfile'
    }
    
  }
  stages {
    stage('Dev') {
      steps {
        echo 'test jenkins file'
      }
    }
    stage('') {
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