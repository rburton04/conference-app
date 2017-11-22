pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        parallel(
          "Dev": {
            echo 'test jenkins file'
            
          },
          "Sonar Qube Tests": {
            echo 'Sonar Qube Tests'
            
          }
        )
      }
    }
    stage('Integration') {
      steps {
        parallel(
          "Integration": {
            echo 'build docker'
            
          },
          "Branch1 BOLT1": {
            echo 'API 1'
            
          },
          "Branch2 BOLT": {
            echo 'API 2'
            
          },
          "BOLT Integration before QA": {
            echo 'Integration'
            
          }
        )
      }
    }
    stage('QA') {
      steps {
        parallel(
          "QA": {
            echo 'QA'
            
          },
          "BOLT Tests": {
            echo 'Report'
            
          },
          "Monitoring": {
            echo 'Monitor QA'
            
          },
          "Reports": {
            echo 'Reports'
            
          }
        )
      }
    }
    stage('PreProd') {
      steps {
        parallel(
          "PreProd": {
            echo 'SPEC TESTING'
            
          },
          "BOLT Tests": {
            echo 'Report'
            
          },
          "Monitoring": {
            echo 'Monitoring'
            
          },
          "Reports": {
            echo 'Reports'
            
          }
        )
      }
    }
    stage('Reports') {
      steps {
        parallel(
          "Reports": {
            echo 'Reports'
            
          },
          "Dashboard Results": {
            echo 'Dashboard Results'
            
          },
          "JIRA Bugs": {
            echo 'Auto Add Jira Bugs'
            
          }
        )
      }
    }
  }
}