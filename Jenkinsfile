
pipeline {

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git url:'git@github.com:manishss/docker-reactjs.git', branch:'dev', credentialsId: 'ba1670bd-cab4-45e3-bc58-10d5e52f3b95'
      }
    }
    
      stage("Build image") {
            steps {
                script {
                    myapp = docker.build("myapp/v1:${env.BUILD_ID}")
                }
            }
        }
    }
}
