pipeline {
    agent any
     stages {
        stage('Build') {
            steps {
                bat "docker build -t myimage2 ."
            }
        }
        stage('Test') {
            steps {
                bat "mvn test"
            }
        }
        stage('Run') {
            steps {
                bat "docker container run -it -d --name tomcatcontainer -p 8080:8080 image2"
            }
        }
    }
}
