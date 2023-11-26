pipeline {
    agent any
    environment {
        // Define environment variables
        DOCKERHUB_CREDENTIALS = credentials('docker-creds') // ID of your Docker Hub credentials in Jenkins
        IMAGE_TAG = "madamanchisathish/sathish-practice:${BUILD_NUMBER}"
        SONAR_URL = "http://sonarqube.infonxt.com:9000/"
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Passed'
                //git branch: 'future', url: 'https://github.com/madamanchisathish/spring-boot.git'
				echo "Clone repository Sucessfully"
            }
        }
		stage('Build and Test') {
            steps {
                // build the project and create a JAR file
                sh 'mvn clean package'
				echo "Maven build Sucessfully"
            }
        }
    }
}
