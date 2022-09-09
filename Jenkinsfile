

pipeline {
    agent any
    stages {
        stage("init") {
            steps {
                ls 'terraform init'
                
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
