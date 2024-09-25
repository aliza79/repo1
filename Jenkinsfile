pipeline{
  agent any
  stages{
    stage("create the container"){
      steps{
        sh " docker run -dp 80:80 --name c1 httpd"
      }
    }
    stage("give access to index file"){
      steps{
        dir('/root/.jenkins/workspace/job1_master'){
                  sh "chmod -R 777 index.html"

        }
      }
    }
    stage("copy file"){
      steps{
        sh "docker cp /root/.jenkins/workspace/job1_master/index.html c1:/usr/local/apache2/htdocs"
      }
    }
  }
}
