pipeline {
    agent any

    stages {
      stage('Deploy App') {
        steps {
          script {
            kubernetesDeploy(configs: "podinfo.yaml", kubeconfigId: "myid")
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

