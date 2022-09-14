
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                git branch: 'dev', changelog: true, poll: true, url: 'https://github.com/Steven18502/Laboratorio2SOA.git'
            }
        }
        stage("build") {
            steps {
                dir('./cloud_function'){
                    sh 'pylint --exit-zero main.py'
                } 
            }
        }
        stage("test") {
            steps {
                echo "testing"
               
            }
        }
        stage("deploy") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'terraform plan'
                    //sh 'terraform apply -auto-approve'
                    sh 'terraform destroy -auto-approve'
                } 
            }
        }
    }   
}
