pipeline{
    agent any
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }
    stages{
        stage ('Cleaning Workspace'){
            steps{
                cleanWs()
            }
        }
        stage ('checkout SCM') {
            steps {
                git 'https://github.com/Minal-git26/k8s-cicd-security-pipeline.git'
            }
        }
        stage ('Compiling Maven Code') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage ('maven Test') {
            steps {
                sh 'mvn test'
            }
