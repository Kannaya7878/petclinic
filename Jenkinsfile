pipeline {
    agent any
    stages {
        stage('Build on k8') {
            steps {
                script {
                    // Print working directory
                    sh 'pwd'
                    
                    // Copy Helm charts
                    sh 'cp -R helm/* .'
                    
                    // List files to verify copy
                    sh 'ls -ltr'
                    
                    // Print working directory again
                    sh 'pwd'
                    
                    // Upgrade or install Helm chart
                    sh '/usr/local/bin/helm upgrade --install petclinic-app ./petclinic'
                }
            }
        }
    }
}
