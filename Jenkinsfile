pipeline {
    agent any

    stages {
        stage('Hello1') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
               /opt/maven38/bin/mvn clean package
                mv target/sparkjava-hello-world-1.0.war target/sparkjava-hello-world-$BUILD_NUMBER.war
                aws s3 cp target/sparkjava-hello-world-$BUILD_NUMBER.war s3://java-projects-cicd/
            }
        }
        stage('Hello3') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Hello4') {
            steps {
                echo 'Hello World'
            }
        }
    }
}
