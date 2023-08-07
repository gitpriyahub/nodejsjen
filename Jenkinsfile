pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'sudo docker build -t srinivas:$Build_Number .'
      }
    }
    stage('Deploy'){
      steps{
        sh 'sudo docker stop'
        sh 'sudo docker run'
        sh 'sudo docker run -itd -p 3000:3000 --name srinivas srinivas:$Build_Number .'
      }
    }

  }

}
