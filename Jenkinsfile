pipeline {
    agent any

    tools {
        maven 'Maven_3.8.7'
        jdk 'JDK_17'
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Rohit-kb07/tomcat.git'
            }
        }

        stage('Build WAR') {
            steps {
                sh 'mvn clean package'
            }
        }

    }
}
