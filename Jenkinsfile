pipeline {
  agent any
  stages{
    stage('Build'){
      steps{
        sh 'sudo docker build -t maqdoom:v$BUILD_NUMBER .'
      }      
    }

    stage('Deploy'){
      steps{
        sh 'sudo docker stop maqdoom'
        sh 'sudo docker rm maqdoom'
        sh 'sudo docker run -itd -p 3000:3000 --name maqdoom maqdoom:v$BUILD_NUMBER'
      }      
    }

  }
}
