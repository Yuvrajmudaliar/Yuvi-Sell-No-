pipeline {

    agent any
    
    tools {
        maven 'Maven'
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building project'
                bat 'mvn -f "pom.xml" clean compile'
            }
        }

        stage('Run Selenium Tests') {
            steps {
                echo 'Running Selenium tests'
                bat 'mvn -f "pom.xml" test'
            }
        }

    }

}
