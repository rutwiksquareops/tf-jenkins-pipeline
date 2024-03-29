pipeline {
    agent any

    environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }

    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code repository
                git 'https://github.com/rutwiksquareops/tf-jenkins-pipeline.git'
            }
        }
        
        stage('Terraform Init') {
            steps {
                // Run terraform init to initialize the working directory containing Terraform configuration files
                sh 'terraform init'
            }
        }
        
    //     stage('Terraform Plan') {
    //         steps {
    //             // Run terraform plan to create an execution plan
    //             sh 'terraform plan -out=tfplan'
    //         }
    //     }
        
    //     stage('Terraform Apply') {
    //         steps {
    //             // Apply the changes described by the execution plan
    //             sh 'terraform apply tfplan'
    //         }
    //     }
    // }
    
    // post {
    //     always {
    //         // Clean up
    //         sh 'rm -rf .terraform'
    //         sh 'rm tfplan'
    //     }
    // }
}
