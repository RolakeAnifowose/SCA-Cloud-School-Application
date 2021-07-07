# SCA-Cloud-School-Application

Pipeline Syntax used: Declarative syntax

pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/RolakeAnifowose/SCA-Cloud-School-Application.git'
                sh 'python sca.py'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
}

Stages:
- Build: I added the link to my github repo and added a command to run my python script
- Test: simple command to echo 'Testing'
- Deploy: added a basic command to echo 'Deploying'
