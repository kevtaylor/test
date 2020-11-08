pipeline {

    options {
        // Build auto timeout
        timeout(time: 60, unit: 'MINUTES')
    }

    // In this example, all is built and run from the master
    agent { node { label 'master' } }

    // Pipeline stages
    stages {

        stage('Test Functionality') {
            steps {

                // Validate kubectl
                sh "kubectl cluster-info"

                // Validate helm
                sh "helm version"
            }
        }
    }
}
