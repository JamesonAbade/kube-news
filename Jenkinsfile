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
                script {
                    docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                        dockerapp.push('latest')
                        dockerapp.push('v1')
                    }
                }
            }
        }
        stage("Deploy Kubernetes") {
            steps {
                sh "echo 'Deploy no Kubernetes'"
                }     
            }         
        } 
    }