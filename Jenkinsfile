pipeline {
  agent any
  stages {
    stage('Build Image') {
      steps {
        sh 'docker build -t myapp . '
      }
    }
    stage('Stop and start Containe') {
      steps {
        sh'''
        docker stop web1
        docker rm web1 
        docker start --name web1 -p 80:80 -d myapp
        '''
      }
     }      
    }  
  } 
