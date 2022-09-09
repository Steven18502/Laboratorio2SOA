
pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'ls'
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
