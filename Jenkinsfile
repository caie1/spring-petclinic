#!/usr/bin/env groovy
properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any

    stages {
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

