pipeline {
    agent any

    stages {
      stage('Deploy App') {
        steps {
          withKubeConfig([credentialsId: 'myid', serverUrl: 'https://192.168.99.100:8443']) {
            sh 'kubectl apply -f podinfo.yaml'
          }
        }
      }
      stage('Main') {
        steps {
          sh 'hostname'
        }
      }
    }
}

