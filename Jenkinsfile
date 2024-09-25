pipeline{
  agent any
  stages{
    stage("create the container"){
      steps{
        sh " docker run -dp 80:80 --name c1 httpd"
      }
    }
    }
  }
