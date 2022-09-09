
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh '$Env:GOOGLE_APPLICATION_CREDENTIALS="lab.json"'
                    sh 'terraform plan'
                    sh 'terraform apply'
                    sh 'terraform destroy'
                }
            }
        }
        stage("build") {
            steps {
                echo "building"
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
