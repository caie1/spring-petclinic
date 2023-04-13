#!/usr/bin/env groovy
properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'cd /var/lib/jenkins/.jenkins/workspace/spring-petclinic_main && ./mvnw package'
            }
        }

        stage('Run') {
            steps {
                sh 'cd /var/lib/jenkins/.jenkins/workspace/spring-petclinic_main && java -jar target/*.jar'
            }
        }
    }
}

