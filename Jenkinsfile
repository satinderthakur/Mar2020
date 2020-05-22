pipeline {
    agent any
     stages {
        stage('Build') {
            steps {
                bat "mvn clean"
            }
        }
        stage('Test') {
            steps {
                bat "mvn test"
            }
        }
        stage('Run') {
            steps {
                bat "mvn package"
            }
        }
        stage('Run') {
            steps {
                bat "docker pull satinderthakur00/test:latest"
             }
        }
        stage('Run') {
            steps {
                bat "docker container run -d -p 8080:8080 satinderthakur00/test"
            }
        }
    }
}
