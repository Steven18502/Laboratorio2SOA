
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                git branch: 'dev', changelog: true, poll: true, url: 'https://github.com/Steven18502/Laboratorio2SOA.git'
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'terraform plan'
                    //sh 'terraform apply -auto-approve'
                    sh 'terraform destroy -auto-approve'
                } 
            }
        }
        stage("build") {
            steps {
                echo "build"
            }
        }
        stage("test") {
            steps {
                echo "testing"
               
            }
        }
        stage("deploy") {
            steps {
               echo "deploying"
            }
        }
    }   
}
