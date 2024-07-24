pipeline {
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'sudo docker build -t maqdoom:v1 .'
      }      
    }

    stage('Deploy'){
      steps{
        sh 'sudo docker run -itd -p 3000:3000 maqdoom:v1'
      }      
    }

  }
}
