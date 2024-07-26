pipeline {
  agent any
  stages {
    stage('Pull SCM') {
      steps {
        git(url: 'https://github.com/moulireddyc/ntsrepo4', branch: 'main', credentialsId: 'ac14a612-5bbe-42ed-9f65-79cd189ad68f')
      }
    }

    stage('Deploy Dev') {
      parallel {
        stage('Deploy Dev') {
          steps {
            echo 'Hello Dev'
          }
        }

        stage('Deply_QA') {
          steps {
            echo 'Hello QA'
          }
        }

      }
    }

    stage('Deply_Prod') {
      steps {
        echo 'Prod Success'
      }
    }

  }
}