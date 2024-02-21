pipeline {
    agent any
    stages {
        stage("Build Docker Image") {
            steps {
                script {
                    dockerapp = docker.build("jamesonabade/kubenews:v1", '-f ./src/Dockerfile ./src')
                }
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