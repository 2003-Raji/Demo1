pipeline {
    agent any
  stages {
    stage ('image build and Push') {
      steps {
        sh '''
            ls
             systemctl status docker
            docker rm -f $(docker images -a -q)
            docker rm -f $(docker ps -a -q)       
            docker build -t sampleapp:1 .
            docker run -d -p 3000:3000 sampleapp:1
        '''
      }
    }