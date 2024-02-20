pipeline {
    agent any
    stages {
        stage("Build Docker Image") {
            steps {
                sh "echo 'Construção da imagem'"
            }
        }
        stage("Push Docker Image") {
            steps {
                sh "echo 'Envio da Imagem'"
                }
            }
        stage("Deploy Kubernetes") {
            steps {
                sh "echo 'Deploy no Kubernetes'"
                }     
            }         
        } 
    }