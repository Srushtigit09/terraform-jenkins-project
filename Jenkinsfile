
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Getting Terraform code from GitHub'
            }
        }

        stage('Terraform Init') {
            steps {
                sh 'terraform init -input=false'
            }
        }

        stage('Terraform Validate') {
            steps {
                sh 'terraform validate'
            }
        }

        stage('Terraform Plan') {
            steps {
                sh 'terraform plan -input=false'
            }
        }
    }
}