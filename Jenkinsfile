pipeline {
  agent any
  stages {
    stage('Build'){
      steps{
        sh 'docker build -t priya:$Build_Number .'
      }
    }
    stage('Deploy'){
      steps{
        sh 'docker stop'
        sh 'docker run'
        sh 'docker run -itd -p 3000:3000 --name priya priya:$Build_Number .'
      }
    }

  }

}
