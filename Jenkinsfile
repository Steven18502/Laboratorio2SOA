
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'terraform plan'
                    sh 'terraform destroy -auto-approve'
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
