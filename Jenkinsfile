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
        stage('Build Docker') {
            steps {
                bat "docker build -t centos/tomcat ."
             }
        }
        stage('Container Run') {
            steps {
                bat "docker container run -d -p 8080:8080 centos/tomcat"
            }
        }
    }
}
