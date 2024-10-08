/* Jenkinsfile for Spring Boot CRUD Application */

pipeline {

    agent any

    tools {
        maven "Maven 3.8.6"
    }

    // Pipeline stages
    stages {

        // Clone the repo from GitHub
        stage ('Clone Repo') {
            steps {
                git branch : 'main',
                url : 'https://github.com/GuptaSwapnesh/SpringBootCRUD_RESTAPI.git'
            }
        }

        // Build the application
        stage ('Maven Build') {
            steps {
                sh "mvn clean package -DskipTest=true"
                archive 'target/*.jar'
            }
        }

        // Application Scanning using SonarQube
        /* stage ('SonarQube Scan') {
            steps {

            }
        } */
    }
}