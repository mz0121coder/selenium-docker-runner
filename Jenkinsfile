pipeline {
  agent any
  stages{

    stage('Run Test'){
        steps{
            sh "docker-compose up"
        }
    }

    stage('Bring Grid Down'){
        steps{
            sh "docker-compose down"
        }
    }
    
    stage('stage-3'){
        steps{
            echo "pushing docker image"
        }
    }
  }

  post {
    always {
        echo "doing clean up"
    }
  }
}