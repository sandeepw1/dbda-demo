pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        docker build -t myapp ./dockerfile
      }
    }
    stage('Stop and start Containe') {
          steps {
            docker stop web1
            docker rm web1 
            docker start --name web1 -p 80:80 -d myapp
          }
      }      
  }
}
  
