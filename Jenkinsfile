pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'git@github.com:caie1/spring-petclinic.git'
            }
        }

        stage('Build') {
            steps {
                sh 'cd spring-petclinic && ./mvnw package'
            }
        }

        stage('Run') {
            steps {
                sh 'cd spring-petclinic && java -jar target/*.jar'
            }
        }
    }
}

