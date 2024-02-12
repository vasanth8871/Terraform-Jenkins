pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
            checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/vasanth8871/Terraform-Jenkins.git']]])            

          }
        }
        
        stage ("terraform init") {
            steps {
                sh ('terraform init') 
            }
        }
        
        stage ("terraform apply") {
            steps {
                sh ('terraform apply --auto-approve') 
           }
        }
    }
}
