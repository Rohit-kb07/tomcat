pipeline {
    agent any

    tools {
        Maven 'Maven_3.8.7'
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

        stage('Deploy WAR') {
            steps {
                // Replace with your actual remote details
                sh 'scp target/my-webapp.war user@your-server:/path/to/tomcat/webapps/'
            }
        }
    }
}
