

pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                dir('./terraform'){
                    sh 'terraform init'
                    sh 'ls'
                    //sh '$Env:GOOGLE_APPLICATION_CREDENTIALS="lab.json"'
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
