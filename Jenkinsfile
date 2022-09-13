
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'terraform plan'
                    sh 'terraform apply -auto-approve'
                    sh 'terraform destroy -auto-approve'
                } 
            }
        }
        stage("build") {
            steps {
                git branch: 'main', changelog: true
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
